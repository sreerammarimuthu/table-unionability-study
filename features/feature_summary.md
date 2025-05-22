# Our Final Feature Set - Used for ML Analysis (All & Aggregated Subsets)   

All the features are associated with the responses to the Table Unionability Questions from the Main Section of the Survey.   

## I. CLICK FEATURES
&emsp;1. FirstClick - Time (in seconds), 0 to 1 (here after global scaling), First time the participant clicked on the screen for that particular question;   
&emsp;2. LastClick - Time (in seconds), 0 to 1 (here after global scaling), Last time the participant clicked on the screen for that particular question;   
&emsp;3. IsSingleClick - 0 or 1, based on whether the participant had a "FirstClick==LastClick";   
&emsp;4. ClickCount - 1 to 46, 0 to 1 (here after global scaling), Number of times the participant clicked on the screen for that particular question;   
&emsp;5. LC-FC - Time (in seconds), Difference between LastClick and FirstClick;   

## II. USER FEATURES
&emsp;6. Browser - 0.5 to 5, mapping the String values to Numerical ones: 'Safari iPhone': 0.5, 'Safari': 1, 'Chrome iPhone': 1.5, 'Chrome': 2, 'Firefox': 3, 'Opera': 4, 'Edge': 5;   
&emsp;7. OS - 1 to 5, mapping the String values to Numerical ones: 'iPhone': 1, 'Linux x86_64': 2, 'Macintosh': 3, 'Ubuntu': 4, 'Windows NT 10.0': 5;   
&emsp;8. Age - 1 or 2, mapping the String values to Numerical ones:(based on participant's age group): '18-24': 1, '25-34': 2;   
&emsp;9. Education - 1 to 3, mapping the String values to Numerical ones:(based on participant's completed level of education): 'High school diploma or equivalent': 1, "Bachelor's degree": 2, "Master's degree": 3;   
&emsp;10. EngProf - 1 to 5, mapping the String values to Numerical ones:(based on participant's English proficiency level): 'Basic': 1, 'Intermediate': 2, 'Proficient': 3, 'Fluent': 4, 'Native speaker': 5;   
&emsp;11. Major - 1 to 5, mapping the String values to Numerical ones:(based on participant's Major): 'Biotechnology': 1, 'Robotics': 2, 'AI': 3, 'Computer Science': 4, 'Data Science': 5;   
&emsp;12. ResolutionLen - 1 to 3, mapping the lengths of Resolution: '7': 1, '8': 2, '9': 3;   

## III. HUMAN LABEL FEATURES
&emsp;13. IsExp - 0 or 1, based on whether the participant gave an explanation with their answer or not;    
&emsp;14. ExplanationsLen - 0 to 1358, String length of the explanations if given or else 0;    
&emsp;15. ExplanationsLen_scaled - 0 to 1, globally scaled version of the ExplanationLen;    
&emsp;16. SurveyAnswer - 0 or 1, answers given by participants for each question ('No' or 'Yes');    

## IV. QUANTIFIED (HUMAN LABELS) FEATURES
&emsp;17. Majority - 0, 0.5 or 1, based on the majority of the SurveyAnswer (Quantified Consensus) for each question in particular (for eg., imagine we have 8 participants answering a question and if most of them (5+) said 'Yes', then Majority=1, similarly for 'No' (Majority=0), if half of them (i.e., 4 said yes and 4 said no, then Majority=0.5);    
&emsp;18. NoCY - 0 to 4, number of times the participant correctly answered 'Yes';     
&emsp;19. NoCN - 0 to 4, number of times the participant correctly answered 'No';    
&emsp;20. Diff_CAns - (-3 to 3), difference between "NoCY" and "NoCN";   

## V. DECISION TIME FEATURES
&emsp;21. DecisionTime - Time (in seconds), 0 to 1 (here after global scaling), amount of time spent by each participant to answer a particular question;    
&emsp;22. OverallSurveyDT - Time (in seconds), 0 to 1 (here after global scaling), amount of time spent by each participant for the entire survey (sum of the time taken to answer all 8 questions, introduction and the questionnaire);     
&emsp;23. MIDT - Mean of Internal DecisionTime (in seconds), among the other responses of a particular "User";    
&emsp;24. ISDT - DecisionTime (in seconds), 0 to 1 (here after internal scaling), i.e., considering only the responses of a particular "User" for each "User";    
&emsp;25. MEDT - Mean of External DecisionTime (in seconds), among the responses of different "Users" answering a particular "Question";    
&emsp;26. ESDT - DecisionTime (in seconds), 0 to 1 (here after external scaling), i.e., considering only the responses of a particular "Question", among different "Users" answering the same question;     
&emsp;27. DecisionTimeFract - 0 to 1 (here after global scaling), ratio of "DecisionTime" with respect to "OverallSurveyDT";     

## VI. CONFIDENCE LEVEL FEATURES
&emsp;28. ConfidenceLevel - 0 to 100 from the Slider, 0 to 1 (here after global scaling), actual reported confidence level by participants for each question;    
&emsp;29. MICL - 0 to 100, Mean of Internal ConfidenceLevel (in seconds), among the other responses of a particular "User";     
&emsp;30. ISCL - ConfidenceLevel, 0 to 1 (here after internal scaling), i.e., considering only the responses of a particular "User" for each "User";    
&emsp;31. MECL - 0 to 100, Mean of External ConfidenceLevel (in seconds), among the responses of different "Users" answering a particular "Question";     
&emsp;32. ESCL - ConfidenceLevel, 0 to 1 (here after external scaling), i.e., considering only the responses of a particular "Question", among different "Users" answering the same question;      
&emsp;33. ConfidenceLevel_Dec - 0 to 1, actual reported ConfidenceLevel in percentage (divided by 100);     
        
## TARGET FEATURE
&emsp;34. ActualAnswer - Labels considered to be correct as per the UGEN benchmarks;      
