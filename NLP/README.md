# Side note: How to use Learning Curves to Diagnose Model Performance 

Reference: https://machinelearningmastery.com/learning-curves-for-diagnosing-machine-learning-model-performance/

- **Train Learning Curve:** Learning curve calculated from the training dataset that gives an idea of how well the model is learning.
- **Validation Learning Curve:** Learning curve calculated from a hold-out validation dataset that gives an idea of how well the model is generalizing.
- **Optimization Learning Curves:** Learning curves calculated on the metric by which the parameters of the model are being optimized, e.g. loss.
- **Performance Learning Curves:** Learning curves calculated on the metric by which the model will be evaluated and selected, e.g. accuracy.


### There are three common dynamics that you are likely to observe in learning curves:
### 
* Underfit.
* Overfit.
* Good Fit.

---

## Underfit Learning Curves:
Underfitting occurs when the model is not able to obtain a sufficiently low error value on the training set.


![](https://i.imgur.com/QQx9f0w.png)
> Description: Example of Training Learning Curve Showing An Underfit Model That Does Not Have Sufficient Capacity.

![](https://i.imgur.com/isecrI5.png)
> Description: Example of Training Learning Curve Showing an Underfit Model That Requires Further Training.

### A plot of learning curves shows underfitting if:
**- The training loss remains flat regardless of training.**
**- The training loss continues to decrease until the end of training.**

---
## Overfit Learning Curves:
Overfitting refers to a model that has learned the training dataset too well, including the statistical noise or random fluctuations in the training dataset.

![](https://i.imgur.com/aMISY95.png)
> Description: Example of Train and Validation Learning Curves Showing an Overfit Model

### A plot of learning curves shows overfitting if:
**-The plot of training loss continues to decrease with experience.**
**-The plot of validation loss decreases to a point and begins increasing again.**

---
## Good Fit Learning Curves:
![](https://i.imgur.com/OGYtYqL.png)
> Description: Example of Train and Validation Learning Curves Showing a Good Fit

### A plot of learning curves shows a good fit if:
**-The plot of training loss decreases to a point of stability.**
**-The plot of validation loss decreases to a point of stability and has a small gap with the training loss.**

---
## Diagnosing Unrepresentative Datasets: 
An unrepresentative validation dataset means that the validation dataset does not provide sufficient information to evaluate the ability of the model to generalize.

This may occur if the validation dataset has too few examples as compared to the training dataset.

There are two common cases that could be observed; they are:
- Training dataset is relatively unrepresentative.
- Validation dataset is relatively unrepresentative.

### Unrepresentative Train Dataset:
![](https://i.imgur.com/KIXmNgx.png)
> Description: Example of Train and Validation Learning Curves Showing a Training Dataset That May Be too Small Relative to the Validation Dataset

### Unrepresentative Validation Dataset:
![](https://i.imgur.com/ZZbKZfZ.png)
> Description: Example of Train and Validation Learning Curves Showing a Validation Dataset That May Be too Small Relative to the Training Dataset

![](https://i.imgur.com/Q9iwIlo.png)
> Description: Example of Train and Validation Learning Curves Showing a Validation Dataset That Is Easier to Predict Than the Training Dataset
