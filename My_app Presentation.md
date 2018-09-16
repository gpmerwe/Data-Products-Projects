ANA215 Exam Predictor App
========================================================
author: Gerrie van der Merwe
date: 2018-09-16
autosize: true

Introduction
========================================================

The ANA215 Exam Predictor App is an application developed by using R Shiny.
The app uses input provided by the user to calculate a prediction for the user's exam mark.

ANA215 is the subject "Introduction to Paleoanthropology" offered at the University of Pretoria (South Africa).


The Input
========================================================
The following input is required for the app:
- Indicate whether the learner is a repeater of not
- Indicate whether any practical were missed
- Numeric input for how many lectures were missed
- Click-up test marks
- Assignment marks
- Semester test marks

The Output
========================================================
The following output components are provided by the app:
- Subject Marks, a table that displays a summary of the subject marks based on the input
- Exam Prediction (Text), indicates the exam admittence and what the predicted exam mark range would be
- Exam Prediction (Graph), shows the exam prediction range over a normal distribution fit of what the class previously achieved. On the next slide you will see an example of the Graph output

Exam Prediction Graph
========================================================

```r
  x <- seq(0, 100, length=1000)
  y <- dnorm(x, mean=44.6, sd=14)
  #plot(x, y, type="l", lwd=1)
  
  plot(y~x, type="l", main="Prediction Range vs Class Distribution" ,xlab="Exam Mark",
       ylab="Density") + abline(v=(45)) + abline(v=(55)) + abline(v=(35))
```

![plot of chunk graph](My_app Presentation-figure/graph-1.png)

```
integer(0)
```



The Model
========================================================
Several model fits were tested and GBM (Gradient Boosting Model) was selected for the app.
The final model was within 10% accuracy when comparing the validation sets' marks vs the predictions.

The range used for the app is the prediction +/- the average absolute error of the model.
This means that the range may not always include the result.

Other Info
========================================================
For more info, please see the documentation provided:
"https://github.com/gpmerwe/Data-Products-Projects/blob/master/README.md"

