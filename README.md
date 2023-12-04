# Deep Learning Analysis and Optimization

### This repository contains a deep learning analysis of charities funded by the Alphabet Soup organization.

The original analysis is contained in the AlphabetSoup.ipynb file. Optimization is contained in the AlphabetSoup_Optimization.ipynb file. Models from both files are contained in the Resources folder in h5 files with the same respective names. Images of model summaries are also included in the Resources folder.


#### Purpose
The purpose of this analysis is to predict whether a charity that has received funding from Alphabet Soup has used its funds effectively. This is denoted in the 'IS_SUCCESSFUL' column of the dataset.

#### Data Preprocessing
* target variable: IS_SUCCESSFUL
* feature variables (note: dummy-encoded categorical variables are denoted with an asterisk (*) ):
    * APPLICATION_TYPE*
    * AFFILIATION*
    * CLASSIFICATION*
    * USE_CASE*
    * ORGANIZATION*
    * STATUS*
    * INCOME_AMT*
    * SPECIAL_CONSIDERATIONS*
    * ASK_AMT

EIN and NAME columns have been removed, since they are used to identify charities.


#### Compiling, Training, and Evaluating the Model

* I decided to use two hidden layers in my initial model, with 50 neurons in the first, and 10 neurons in the second. I decided to use ReLU as my activation function, since I read up on various activation functions, and ReLU is generally preferred.

* I was able to achieve an accuracy score of about 0.73 with this model, not quite reaching the target of 0.75.

* I attempted to increase model performance by first by adding some nodes to the second layer, and dropping some excess columns, such as APPLICATION_TYPE_Other, CLASSIFICATION_Other, and SPECIAL_CONSIDERATIONS_Y. This improved performance to 0.736.

* For my second attempt, I added a third hidden layer. This improved performance to 0.7388.

* For my third attempt, I tested varying activation functions, changing the second and third layers to sigmoid and tanh activation functions, respectively. I also increased the number of epochs to 150. This actually led to a decrease in performance, giving 0.734 accuracy.


#### Summary

In the end, I was not able to achieve the target accuracy score. In the future, I would try a simpler classification model, as the neural net may be overcomplicating things. I would also experiment with different count cutoffs for certain categorical variables, as the cutoffs that I chose may not have been optimal.



