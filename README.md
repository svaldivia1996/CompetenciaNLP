# CompetenciaNLP
Named Entity Recognition (NER) in Spanish

 

A named entity is a real-world object, such as persons, locations, organizations, products, etc., that can be denoted with a proper name. It can be abstract or have a physical existence. Named Entity Recognition is the task of locating and classifying Named Entities in unstructured text.

In this assignment, your task is to apply sequence labeling techniques focused on locating and classifying appearances of Named Entities in unstructured Spanish text. The corpus corresponds to medical referals from diagnosis on Chilean waiting list. Specifically, given a sentence, each word in it must be classified into 5 classes:

    Disease
    Body_part
    Medication
    Procedure
    Family_Member

In addition, since there are entities that are composed of more than one word, an additional notation will be used to distinguish whether any detected entity is initial or intermediate. For this, the previous classes will be complemented with the following tags:

    Beggining (B)
    Inside(I)

Its use is relatively simple: Given a word, first it is denoted if it is initial (B) or intermediate (I), then a guide is added and finally, its corresponding class. If there is no Named Entity, simply return the class (O). For example, a correct NER would be the following:

        PACIENTE O
        PRESENTA O
        FRACTURA B-Disease
        CORONARIA I-Disease
        COMPLICADA I-Disease
        EN O
        PIE B-Body_Part
        IZQUIERDO I-Body_Part
        . O
        SE O
        REALIZA O
        INSTRUMENTACION B-Procedure
        INTRACONDUCTO I-Procedure
        . O

As is usual for data mining competitions involving a supervised learning problem, gold-standard labels are only given for the training data. Once a classifier has been trained, it can be used to obtain classifications for the test data. These classifications are then submitted and compared to the hidden actual classifications. A leaderboard is established by comparing the submitted classifications to the actual ones using some performance measure.

Data: Training and target datasets are provided in the following links:

    train

    dev

    test

 

An essential part of this task is to make a submission by generating predictions using python and library reviewed in classes.
