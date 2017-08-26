Experimental Design
---

Basics to get started :

Why you should care about experimental design ?

* Exemple study : Genomic signatures to guide the use of chemoterapeutics

The first thing to be aware of when performing any sort of an experimental deisgn or data science project is to care about the analysis plan

To share your data with small amounts, GitHub is ok

For larger amounts, you might go on *Figshare.com*

Recomendation of a data plan : The Leek group guide to data sharing available here: https://github.com/jtleek/datasharing

--

* The First thing you need when you perform an experiment is **formulate your question in advance** (exemple AB testing Barack Obama campaign)

## Inference

This bring sus to the key idea of a large component of data science which is statistical inference : http://www.gs.washington.edu/academics/courses/akey/56008/lecture/lecture2.pdf

THey use inferential statistics to decide if implement new versions :

3 scenarios of results :

Scenario 1 very variable answer

Scenario 2 :  smaller variability but without huge benefit

Scenario 3 : SMall variability and huge difference in benefit

Another important issue, is the issue of Confounding :

in a particural study you mesure both shoe size and literacy, and you are looking for correlation between shoe size and literacy, and you can find a correlation: people with smallshoes tend to have less literacy

But you are missing that AGE is actually the variable that's causing this relationship!!! (Babies have less literacy!!!) : *pay attention to what are the other variables that might be causing a relationship!*

Real exemple : consumption of chocolate vs Nobel prize laureate!! 

This is often called "Spurious correlation" and that's why you have often the phrase "correlation is not causation"

Why to deals with potential confounders :

1 Fix some variables (fix Obama 2014 on the website > 2012)

2 Stratify : if you test sign up phrases and have two website volors, use both phrases equally on both

3 If you can fix or stratify a varible, randomize it : this let us balance a confoundig variable

## Prediction

We have individuals that come in and we mesure something about their genomeand we want to predict whether they're going to respond to chemotherapy or not. SO we collect these individuals and collect observations from people that respon well to chemo and did not respond.

And then we want to build a predictive function : if we get a new individual, to predict if he's responding or not to chemo : so we still have to deal with **probability**, **sampling** and **potential confounding variables** 

Prediction is more challenging than inference : for a variable, you need distributions of population to be a bit more separated :so it's  important to pay attention to the relative size of effects when considering prediction vs inference

For prediction there's several key quantities thet we need to be aware of (exemple of a medical test scenario) :

* Sensitivity (proability you have a postive test, given you have the disease)
* Specificity (proability you have a negative test, given you don't have the disease)
* Positive predictive value (probability you have a disease, given you have a positive test)
* Negative predictive value (probability you don't have a disease, given you have a negative test)
* Accuracy (ptobability you are correct in the outcome, regardles is positive or negative)

## Be aware in data dredging

https://xkcd.com/882/

You have to pay attention of data dredging when you deal with (big or not) data

IN SUMMARY : 

* good experiments **have replications**, so you can **measure variability** and compare it to the signal they were loking for, and they **generalize to the problem that you care about** ... and they **are transparents**

* **prediction is not inference** : both are important, but it dependsn on you application

* **be aware of data dredging**
