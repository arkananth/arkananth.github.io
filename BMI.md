BMI Calculator Project
===================================================================
author: Ananth
date: 25-11-2014

What is Body Mass Index?
=================================

The Body Mass Index (BMI) is a measure of body fat based on height and weight that applies to adult men and women. Regarding the BMI measure, the World Health Organization (WHO) proposes the following classification:

BMI <18.5 : Underweight

BMI [18.5-24.9] : Normal weight

BMI [25-29.9] : Overweight

BMI >=30 : Obesity


How is it calculated?
=================================

There is a formula for calculating the BMI measure. The formula is the following:

BMI = weight(kg) / height(metres)2

Example:


```r
weight = 75
height = 1.8
BMI <- weight/height^2
BMI
```

```
[1] 23.14815
```

Diagnostic
===============

The function use for calculating the diagnostic is the following:


```r
diagnostic_f <- function(weight, height) {
    BMI_value <- weight/(height^2)
    ifelse(BMI_value < 18.5, "underweight", ifelse(BMI_value < 25, "normal weight", 
        ifelse(BMI_value < 30, "overweight", "obesity")))
}
```
For our example (weight=75 kg and height=1.80 m) the diagnostic would be:


```r
diagnostic_f(75, 1.8)
```

```
[1] "normal weight"
```

Conclusion
=============

The BMI correlates reasonably well with their level of body fat.

However, BMI is only a proxy for body fatness. other factors such as fitness, ethnic origin and puberty can alter the relation between BMI and body fatness and must be taken into consideration.

