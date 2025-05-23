# Our Final Feature Set - Used for ML Analysis (Aggregated Subsets)   

All the features are associated with the responses to the Table Unionability Questions from the Main Section of the Survey.   

## I. CLICK FEATURES

These features capture the participant’s click behavior and interaction timing on each question. They helped us characterize engagement patterns, and attention of the participant.    

- FirstClick - Time (in seconds), 0 to 1 (here after global scaling), First time the participant clicked on the screen for that particular question;   
- LastClick - Time (in seconds), 0 to 1 (here after global scaling), Last time the participant clicked on the screen for that particular question;   
- IsSingleClick - 0 or 1, based on whether the participant had a "FirstClick==LastClick";   
- ClickCount - 1 to 46, 0 to 1 (here after global scaling), Number of times the participant clicked on the screen for that particular question;   
- LC-FC - Time (in seconds), Difference between LastClick and FirstClick;   

## II. USER FEATURES

These describe the participant’s metadata from Qualtrics along with self-reported background information. All of them are categorical features, we included them in the experiment, to check if it improves model performance.   

- Browser - 0.5 to 5, mapping the String values to Numerical ones: 'Safari iPhone': 0.5, 'Safari': 1, 'Chrome iPhone': 1.5, 'Chrome': 2, 'Firefox': 3, 'Opera': 4, 'Edge': 5;  
- OS - 1 to 5, mapping the String values to Numerical ones: 'iPhone': 1, 'Linux x86_64': 2, 'Macintosh': 3, 'Ubuntu': 4, 'Windows NT 10.0': 5;   
- Age - 1 or 2, mapping the String values to Numerical ones:(based on participant's age group): '18-24': 1, '25-34': 2;   
- Education - 1 to 3, mapping the String values to Numerical ones:(based on participant's completed level of education): 'High school diploma or equivalent': 1, "Bachelor's degree": 2, "Master's degree": 3;   
- EngProf - 1 to 5, mapping the String values to Numerical ones:(based on participant's English proficiency level): 'Basic': 1, 'Intermediate': 2, 'Proficient': 3, 'Fluent': 4, 'Native speaker': 5;   
- Major - 1 to 5, mapping the String values to Numerical ones:(based on participant's Major): 'Biotechnology': 1, 'Robotics': 2, 'AI': 3, 'Computer Science': 4, 'Data Science': 5;   
- ResolutionLen - 1 to 3, mapping the lengths of Resolution: '7': 1, '8': 2, '9': 3;   

## III. HUMAN LABEL FEATURES

These features reflect the participant’s survey answers and other associated inputs, including explanations and their lengths, capturing how much thought or detail was given to the response.  

- IsExp - 0 or 1, based on whether the participant gave an explanation with their answer or not;  
- ExplanationsLen - 0 to 1358, String length of the explanations if given or else 0;  
- ExplanationsLen_scaled - 0 to 1, globally scaled version of the ExplanationLen;  
- SurveyAnswer - 0 or 1, answers given by participants for each question ('No' or 'Yes');    

## IV. QUANTIFIED (HUMAN LABELS) FEATURES

These features quantify group-level correctness and consensus for each question, helping capture answer patterns, agreement levels, and confidence across participants.   

- Majority - 0, 0.5 or 1, based on the majority of the SurveyAnswer (Quantified Consensus) for each question in particular (for eg., imagine we have 8 participants answering a question and if most of them (5+) said 'Yes', then Majority=1, similarly for 'No' (Majority=0), if half of them (i.e., 4 said yes and 4 said no, then Majority=0.5);   
- NoCY - 0 to 4, number of times the participant correctly answered 'Yes';  
- NoCN - 0 to 4, number of times the participant correctly answered 'No';
- Diff_CAns - (-3 to 3), difference between "NoCY" and "NoCN";   

## V. DECISION TIME FEATURES

This feature group captures temporal patterns in decision-making, both at the individual level and in comparison with others. They include internal and external scaling of decision times.    

- DecisionTime - Time (in seconds), 0 to 1 (here after global scaling), amount of time spent by each participant to answer a particular question;    
- OverallSurveyDT - Time (in seconds), 0 to 1 (here after global scaling), amount of time spent by each participant for the entire survey (sum of the time taken to answer all 8 questions, introduction and the questionnaire);     
- MIDT - Mean of Internal DecisionTime (in seconds), among the other responses of a particular "User";    
- ISDT - DecisionTime (in seconds), 0 to 1 (here after internal scaling), i.e., considering only the responses of a particular "User" for each "User";    
- MEDT - Mean of External DecisionTime (in seconds), among the responses of different "Users" answering a particular "Question";    
- ESDT - DecisionTime (in seconds), 0 to 1 (here after external scaling), i.e., considering only the responses of a particular "Question", among different "Users" answering the same question;     
- DecisionTimeFract - 0 to 1 (here after global scaling), ratio of "DecisionTime" with respect to "OverallSurveyDT";     

## VI. CONFIDENCE LEVEL FEATURES

These features represent the self-reported confidence for each decision, same as earlier, both at the individual level and in comparison with others. They include internal and external scaling of decision times.    

- ConfidenceLevel - 0 to 100 from the Slider, 0 to 1 (here after global scaling), actual reported confidence level by participants for each question;    
- MICL - 0 to 100, Mean of Internal ConfidenceLevel (in seconds), among the other responses of a particular "User";     
- ISCL - ConfidenceLevel, 0 to 1 (here after internal scaling), i.e., considering only the responses of a particular "User" for each "User";    
- MECL - 0 to 100, Mean of External ConfidenceLevel (in seconds), among the responses of different "Users" answering a particular "Question";     
- ESCL - ConfidenceLevel, 0 to 1 (here after external scaling), i.e., considering only the responses of a particular "Question", among different "Users" answering the same question;      
- ConfidenceLevel_Dec - 0 to 1, actual reported ConfidenceLevel in percentage (divided by 100);     
        
## TARGET FEATURE

- ActualAnswer - Labels considered to be correct as per the UGEN benchmarks;      
