Our Final Feature Set - Used for ML Analysis (All & Aggregated Subsets)   
All the features are associated with the responses to the Table Unionability Questions from the Main Section of the Survey.   

I. *CLICK FEATURES:*   
    1. FirstClick - Time (in seconds), First time the participant clicked on the screen for that particular question;   
    2. LastClick - Time (in seconds), Last time the participant clicked on the screen for that particular question;   
    3. IsSingleClick - 0 or 1, based on whether the participant had a "FirstClick==LastClick";   
    4. ClickCount - Number of times the participant clicked on the screen for that particular question;   
    5. LC-FC - Time (in seconds), Difference between LastClick and FirstClick;   
    
II. USER FEATURES:   
    6. Browser - 0.5 to 5, Mapping the String values to Numerical ones: 'Safari iPhone': 0.5, 'Safari': 1, 'Chrome iPhone': 1.5, 'Chrome': 2, 'Firefox': 3, 'Opera': 4, 'Edge': 5;   
    7. OS - 1 to 5, Mapping the String values to Numerical ones: 'iPhone': 1, 'Linux x86_64': 2, 'Macintosh': 3, 'Ubuntu': 4, 'Windows NT 10.0': 5;   
    8. Age - 1 or 2, Mapping the String values to Numerical ones:(based on participant's age group): '18-24': 1, '25-34': 2;   
    9. Education - 1 to 3, Mapping the String values to Numerical ones:(based on participant's completed level of education): 'High school diploma or equivalent': 1, "Bachelor's degree": 2, "Master's degree": 3;   
    10. EngProf - 1 to 5, Mapping the String values to Numerical ones:(based on participant's English proficiency level): 'Basic': 1, 'Intermediate': 2, 'Proficient': 3, 'Fluent': 4, 'Native speaker': 5;   
    11. Major - 1 to 5, Mapping the String values to Numerical ones:(based on participant's Major): 'Biotechnology': 1, 'Robotics': 2, 'AI': 3, 'Computer Science': 4, 'Data Science': 5;   
    12. ResolutionLen - 1 to 3, Mapping the lengths of Resolution: '7': 1, '8': 2, '9': 3;   
    
III. HUMAN LABEL FEATURES:   
    13. IsExp - 
    14. ExplanationsLen - 
    15. ExplanationsLen_scaled - 
    16. SurveyAnswer - 

IV. QUANTIFIED (HUMAN LABELS) FEATURES:
    17. Majority - 
    18. NoCY - 
    19. NoCN - 
    20. Diff_CAns - 

V. DECISION TIME FEATURES:
    21. DecisionTime - 
    22. OverallSurveyDT - 
    23. MIDT - 
    24. ISDT - 
    25. MEDT - 
    26. ESDT - 
    27.DecisionTimeFract - 


VI. CONFIDENCE LEVEL FEATURES:
    28. ConfidenceLevel - 
    29. MICL - 
    30. ISCL - 
    31. MECL - 
    32. ESCL - 
    33. ConfidenceLevel_Dec - 

TARGET FEATURE:
    34. ActualAnswer - Labels considered to be correct as per the UGEN benchmarks;
