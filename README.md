# IE2064-competition

This repo contains files relevant to the IE2064 course competition, specifically for Alex Federspiel and Evan Miu.

The final predictions are contained in the file `competition-test-outcome.csv`.
Also, trained model parameters are stored in `competition.Rdata`.
If you want to run the `Competition_Models.Rmd` script, it would be much faster if you download the `.Rdata` image.
Change line 13 to
```r
retrain_model <- FALSE
```
in order to use the already-trained models.
The knitted results are already contained in the `Competition_Models.pdf` file as well.
In the end, a GBM model with 500 trees, a limit of 10 decisions, a regularization of 0.075, and a node cutoff of 10 observations provided the best RMSE in our training data.
Testing all models on the never-before-seen validation data confirmed our 10-fold cross-validated RMSE's developed from the training data.
The final outcomes were predicted using the above-mentioned GBM model.
