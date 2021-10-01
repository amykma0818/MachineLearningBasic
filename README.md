# ML & Stats Basic
### 1. What is standard error of mean, how to compute it, and how to interpret it?
* Standard error is the standard deviation of the sampling distribution of the mean, $`s = σ/\sqrt{n}`$. It refers to the standard deviation of the distribution of sample means
taken from a population. The smaller the standard error, the more representative the sample will be of the overall population (a measurement for the
spread, the smaller the spread, the more accurate the dataset). 

### 2. [How to compute standard error of median in a simple way?](https://towardsdatascience.com/how-to-estimate-the-standard-error-of-the-median-the-bootstrap-strategy-ed09cccb838a)
* Bootstrap. For example randomly select data with replacement from the dataset for 10000 times, so that we can get 10000 new datasets. Consider median as the resampling statistic, get median of each bootstrap dataset and
calculate the standard error from these 10000 median $`\sqrt{(Σ(x_i - \mu(median))^2/(n-1))}/\sqrt{n}`$.
While if the sample is drawn from a normal distribution with large sample size, $`se(median) = 1.2533*se(mean)`$.

### 3. Two-sample t-test vs. paired t-test, which one has higher statistical power?
* Depend on the degree of freedom. Degrees of freedom (DOF) equals your sample size minus the number of parameters you need to calculate during an analysis. Higher DOF generally mean larger sample sizes or fewer unknown parameters, a higher DOF means more power to reject a false null hypothesis and find a significant result.
* The DOF of (unpaired) two-sample t-test is ($`n_1+n_2-2`$)
* The DOF of paired t-test, which is equivalent to one-sample t-test, is ($`n-1`$).

### 4. Explain the differences between two statistical tests called t-tests and z-tests. 
In your explanation, create two examples of when you would use the tests, one scenario for t-tests and one scenario for z-tests. This will help highlight real life situations when one test would be utilized over the other.
#### Solution:
Both t-tests and z-tests are forms of hypothesis testing. In general, choosing which one to use between the two (assuming population is normally distributed) is more dependent on the sample size as well as whether or not we're able to obtain the population's standard deviation. Both t-scores and z-scores will have an associated p-value. z-test is used when sample size is large, or the population variance is known. t-test is used when sample size is small and population variance is unknown.

A z-test is used for testing the mean of a population vs. a constant, or comparing the means of two populations, with large (n ≥ 30) samples whether you know the population standard deviation or not. It is also used for testing the proportion of some characteristic versus a standard proportion, or comparing the proportions of two populations.

Examples:

* Comparing the average engineering salaries of men versus women.
* Comparing the fraction defectives from 2 production lines.

A t-test is used for testing the mean of one population against a constant or comparing the means of two populations if you do not know the populations’ standard deviation and when you have a limited sample (n < 30). If you know the populations’ standard deviation and the sample size is 30 or above, you may use a z-test.

Examples:
* Measuring the average diameter of shafts from a certain machine when you have a small sample.
* Comparing avg engineering salaries of men versus women when you have a small (less than 30) sample

### 5. What is Analysis of Variance (ANOVA)? [What's the difference between F-test and ANOVA?](https://statisticsbyjim.com/anova/f-tests-anova/)

### 6. What's supervised algorithm? 
* Supervised learning is the use of examples of known correct answers to train the network. A process in which data and its one-to-one correspondence are known, a prediction model is trained, and input data is mapped to a label.
* Common application scenarios for supervised learning such as classification and regression.
* Common supervised machine learning algorithms include Support Vector Machine (SVM), Naive Bayes, Linear Regression, Logistic Regression, K-Nearest Neighborhood (KNN), Decision Tree (including Random Forest and AdaBoost), and Linear Discriminant Analysis (LDA). Deep Learning is also presented in the form of supervised learning.

### 7. In statistical hypothesis testing, explain the difference between Type I and Type II error.
* Type I error is defined as 'the rejection of a true null hypothesis (also known as a "false positive" finding)', whereas Type II error is defined as 'failing to reject a false null hypothesis (also known as a "false negative" finding)'. In other words, Type I error is claiming something has happened when it has not, while Type II error is claiming nothing has happened when it has.
* For example, a model telling someone they have cancer when they do not is Type I error, while a model telling someone they do not have cancer when they in fact do is Type II error. You should also be prepared to think through when you might want to bias your model towards one type of error vs. the other.
### 8. What is Naive Bayes' theorem, and why is it considered 'naive'? Why is it often used in practical applications rather than trying to implement an algorithm based on Bayes' Theorem (non-naive)?
* Naive Bayes is a machine learning implementation of Bayes' Theorem. In short, Bayes' Theorem is an algorithm that describes the probability of an event, based on prior knowledge of conditions that might be related to the event. In other words, it describes how to update the probability of an event given new evidence.
* Naive Bayes is 'naive' because while it uses conditional probability to make classifications, the algorithm assumes that all features of a class are independent. This is considered naive because, in reality, it is not often the case. Naive Bayes is often used over bayesian classifiers since the latter is very difficult to compute. Naive Bayes offers a good approximation that runs much quicker, is easier to follow, and works just fine for many problems.



