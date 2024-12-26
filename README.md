# Stepwise Regression:

## Building A model with more than one Independent Variable
> When you have more than one independent variable (IV), such as x1, x2, x3, x4, x5, x6 etc, and y (dependent variable). They are many and we may decide to drop some of the IV.
> Why do we need to drop some, why can't we use all the predictors at once.
> 
> __Here are some Reasons we should consider dropping some:__
> 1. Garbage in Garbage out. Do not just use any how variables in your model as it can affect its efficiency
> 2. Selecting the ones that contribute to prdicting is better than having a thousand of them that do not all predict something.

## Stepwise Regression
Stepwise regression is a method of fitting regression models in a step-by-step manner, adding or removing predictors based on specific criteria, to identify a subset of variables that best explains the variation in the response variable. It can be used for both linear and logistic regression. It refers to Number 2,3 & 4. Sometimes people refer to Stepwise regression as Bidirectional Elimination

## Five Methods to Building A Model
> 1. + Use-In
>    + In this methos, you use all the variables. This method is use when you have prior knowledge of the variable, and you know they are good predictors or you are provided with the variables to just build the model
>    + You can adopt this method if you are preparing for backward elimination

> 2. + Backward Elimination:
> + Start with all predictors in the model.
> + Remove predictors one by one based on their insignificance (e.g., largest p-value or lowest F-statistic).
> + Stop when all remaining predictors are significant.
>   
>      #### Step By Step
>      + Step 1: Select a significant level to stay in the model (SL=0.05)
>      + Sep2: Fit the full model with all possible predictors. 
>      + Step3: Consider the predictor with the highest P-Value. if P> SL, go to step 4, otherwise FIN (your model is ready)
>      + Step4: Remove the predictor
>      + Step5: Fit model without the variable
>        Note: after removing the predictors, you have to rebuild the model or fit again as its going to have different coefficient and constant too is going to be different
>        Once you remove a variable, it affects all other variable reason to rebuild model

> 3. __Forward Selection:__
> + Start with no predictors in the model.
> + Add predictors one by one based on their significance (e.g., smallest p-value or highest F-statistic).
> + Stop when no more significant predictors can be added.

> ### Steps
> 1. Select a significant level to enter the model (SL = 0.05)
> 2. Fit all simple regression model (y~Xn). Slect the one with the lowest p-value
> 3. keep this variable and fit all possible models with one extra predictor added to the one you already have
> 4. Consider the predictor with the lowest p-value. If p > SL, go to step3, otherwise go to finish
> 
> ### Note: you grow the model with one variable at a time. Once the P > SL, you finish the model because no more variable with lowest p-value, If you just added a variable that is insignificant, go back to the previous model not the new one.

> __Bidirectional Elimination (Stepwise Selection):__
> + Combines forward selection and backward elimination.
> + Add and remove predictors simultaneously, evaluating at each step whether to include or exclude a variable.
>   
>   __Steps for Bidirectional Elimination:__
>   1. Select a significance level to enter and to stay in the model e.g SLENTER = 0.05, SLSTAY = 0.05
>   2. Perform the next step of Forward selection (new variables must have P < SLENTER to enter)
>   3. Perform all steps of backward elimination (Old variables must have P < SLSTAY to stay)
>   4. No new variables can enter and no old variable can exit (proceed to finish because your model is ready)


> 5. + Score Comparison
>    + All possible Models
>    + It is the more thorough approach but takes lot of resources.
>    Steps:
>    + 1. You select a criterion of goodness of fit (e.g Akaike Criterion)
>    + 2. Construct all possible regression models. 2(power n)- 1 total combinations
>    + 3. Select the one with the best criterion
>      4. model is ready e.g if you have 10 columns in your dataset, it means you will have 1023 models. That's a lot


## Which is fastest of all types?
Backward Elimination, It's a much faster approach

