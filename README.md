# Building_MLR_Model

## Building A model with more than one Independent Variable
> When you have more than one independent variable (IV), such as x1, x2, x3, x4, x5, x6 etc, and y (dependent variable). They are many and we may decide to drop some of the IV.
> Why do we need to drop some, why can't we use all the predictors at once.
> 
> __Here are some Reasons we should consider dropping some:__
> 1. Garbage in Garbage out. Do not just use any how variables in your model as it can affect its efficiency
> 2. Selecting the ones that contribute to prdicting is better than having a thousand of them that do not all predict something.

## Five Methods to Building A Model
> 1. + Use-In
>    + In this methos, you use all the variables. This method is use when you have prior knowledge of the variable, and you know they are good predictors or you are provided with the variables to just build the model
>    + You can adopt this method if you are preparing for backward elimination

> 2. + Backward Elimination:
>      #### Step By Step
>      + Step 1: Select a significant level to stay in the model (SL=0.05)
>      + Sep2: Fit the full model with all possible predictors
>      + Step3: Consider the predictor with the highest P-Value. if P> SL, go to step 4, otherwise FIN
>      + Step4: Remove the predictor
>      + Step5: Fit model without the variable
>      + 
> 3. + Forward Selection
> 4. + Bidirectional Elimination
> 5. + Score Comparison

### Stepwise Regression
> It refers to Number 2,3 & 4. Sometimes people refer to Stepwise regression as Bidirectional Elimination
