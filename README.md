## Week 2: Building ML Models
Baseline (always "stay"): accuracy 
 Logistic Regression: recall --> 0.567, AUC --> 0.8422
Random Forest: recall --> 0.568, AUC  --> 0.8420
Moving the threshold from 0.5 to 0.20 caught 108 more churners.
 The right threshold is a business decision, not a default.
Biggest lesson: A model that predicts "no one leaves" is 73.5 % accurate and catches zero churners. So I stopped trusting accuracy.
