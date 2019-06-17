# Grab-AI-Challenges-Safety
Project for Grab AI Challenges - Making a model to predict safety in trips 

In this project, I am using R programming language with Rstudio. 
So to run the program , install and open the latest release of R and Rstudio.
with rmarkdown package installed. *The detailed instruction in  the rmd notebook file.

Feature Extraction
I create a feature based on basic knowledge of the vector, speed, and the law of pyshics.
Such as;
 - distance = second(time)*Speed.
 - length of vector = square root of the sum square of its component.
    sqrt(x^2+y^2+z^2)
Then, trying to extract the statics from each feature. Mean, mode, median, sd.

In this model, I use ensemble approach method, Multistage Combination Method. 
Multistage Combination is method that use a serial approach where the next 
base-learner is trained with or tested only the instance where the previous 
base-learners are not accurate enough. [1] ("Introduction to Machine Learning", Alpaydn, 2010).

Multistage Combination : 
1. The first-stage Learner is Logistic Regression
2. The Second-stage Learner is Logistic Regression

The Overall Performance in this model with Cross Validataion
70% training and 30% testing data.

Confusion Matrix and Statistics

          Reference
Prediction    0    1
         0 4391   79
         1   81 1443
                                          
               Accuracy : 0.9733          
                 95% CI : (0.9689, 0.9772)
    No Information Rate : 0.7461          
    P-Value [Acc > NIR] : <2e-16          
                                          
                  Kappa : 0.9296          
                                          
 Mcnemar's Test P-Value : 0.937           
                                          
            Sensitivity : 0.9481          
            Specificity : 0.9819          
         Pos Pred Value : 0.9469          
         Neg Pred Value : 0.9823          
             Prevalence : 0.2539          
         Detection Rate : 0.2407          
   Detection Prevalence : 0.2543          
      Balanced Accuracy : 0.9650          
                                          
       'Positive' Class : 1               
                                          


 AUC 
Setting levels: control = 0, case = 1
Setting direction: controls < cases
Area under the curve: 0.965
