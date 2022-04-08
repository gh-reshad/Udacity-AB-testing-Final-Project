# Udacity-AB-testing-Final-Project

## Table of Contents

- Experiment Description
- Metric choice
- Sizing
- Analysis

---
## Experiment Description
At the time of this experiment, Udacity courses currently have two options on the course overview page: "start free trial", and "access course materials". If the student clicks "start free trial", they will be asked to enter their credit card information, and then they will be enrolled in a free trial for the paid version of the course. After 14 days, they will automatically be charged unless they cancel first. If the student clicks "access course materials", they will be able to view the videos and take the quizzes for free, but they will not receive coaching support or a verified certificate, and they will not submit their final project for feedback.

In the experiment, Udacity tested a change where if the student clicked "start free trial", they were asked how much time they had available to devote to the course. If the student indicated 5 or more hours per week, they would be taken through the checkout process as usual. If they indicated fewer than 5 hours per week, a message would appear indicating that Udacity courses usually require a greater time commitment for successful completion, and suggesting that the student might like to access the course materials for free. At this point, the student would have the option to continue enrolling in the free trial, or access the course materials for free instead. [This screenshot](https://drive.google.com/file/d/0ByAfiG8HpNUMakVrS0s4cGN2TjQ/view?resourcekey=0-6_dPu8BRM1XlRgV51nIbtA) shows what the experiment looks like.

### Null Hypothesis
The null hypothesis is that by taking this approach udacity might not be able to effectively reduce the number of early cancellation.

### Alternative Hypothesis
The alternative hypothesis is that this approach might be effective in reducing the number of frustrated students who left the free trial beacause they did not have enough time.

---
# Metric Choice

..* Invariant metrics

Invariant metrics are the ones that used for sanity checks and will remain invariat throughout the experiment

_Number of cookies_: That is, the number of unique cookies to view the course overview page

_Number of clicks_: That is, the number of unique cookies to click the "Start free trial" button (which happens before the free trial screener is trigger)

_Click through probability_: That is, number of unique cookies to click the "Start free trial" button divided by number of unique cookies to view the course overview page

..* Evaluation metrics

Evaluation metrics are those the one we care about. The metrics that we use to run the experiment and make a decision based on.

_Gross conversion_: That is, number of user-ids to complete checkout and enroll in the free trial divided by number of unique cookies to click the "Start free trial" button

_Retention_: That is, number of user-ids to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by number of user-ids to complete checkout

_Net conversion_: hat is, number of user-ids to remain enrolled past the 14-day boundary (and thus make at least one payment) divided by the number of unique cookies to click the "Start free trial" button

# Sizing

..* Calculating the standard deviation

Udacity has provided the baseline values for each metric. [This spreadsheet](https://docs.google.com/spreadsheets/d/1MYNUtC47Pg8hdoCjOXaHqF-thheGpUshrFA21BAJnNc/edit#gid=0)

For each evaluation metric, calculating the standard deviation given a sample size of 5000 cookies visiting the course overview page.
