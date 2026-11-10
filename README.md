# econ3916-lab15-bias-variance
# The Bias-Variance Tradeoff: Choosing How Flexible a Model Should Be

## Objective
I wanted to see how a polynomial model's degree affects its error on new data, and to test ways of choosing a degree when the true curve is unknown.

## Methodology
- I set up a simulated world with a known true curve so I could measure error against the truth directly.
- At each of six polynomial degrees, I fit the model to 200 fresh samples and split its error into bias squared and variance.
- For degrees 1 to 15, I compared training error with error on 2,000 new points, and I noted the degree where the held-out error was lowest.
- I used 5-fold cross-validation to choose a degree, and I looked at how much the error changed from one fold to the next.
- I used nested cross-validation to check whether the smallest CV error is a fair estimate of the error on new data.
- I wrote a small function, `kfold_mse()`, that returns the k-fold CV error for any degree and number of folds, and I checked it with 10 folds.
- *(Take-home Challenge)* I looked at held-out error for degrees past the interpolation point.

## Key Findings
- **Variance:** [YOUR VALUE] at degree 5 and [YOUR VALUE] at degree 15.
- **Held-out error:** The lowest held-out error on the 2,000 new points came at degree [YOUR VALUE].
- **5-fold CV:** Cross-validation chose degree [YOUR VALUE], with a CV MSE of [YOUR VALUE].
- **Nested CV:** The nested CV estimate of error on new data was [YOUR VALUE], which I compared with the smallest CV MSE above.
- **10-fold CV with `kfold_mse()`:** The CV MSE was [YOUR VALUE] for degree 4 and [YOUR VALUE] for degree 5.
- *(Take-home Challenge)* **Past the interpolation point:** [YOUR RESULT]
