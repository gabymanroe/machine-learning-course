**Question 1**<br>
This example is adapted from a real production application, but with details disguised to protect confidentiality.<br>
![image](https://github.com/user-attachments/assets/226e4699-a67f-4e09-80a1-f777e0ef7d4e)<br>
You are a famous researcher in the City of Peacetopia. The people of Peacetopia have a common characteristic: they are afraid of birds. To save them, you have to build an algorithm that will detect any bird flying over Peacetopia and alert the population.<br>
The City Council gives you a dataset of 10,000,000 images of the sky above Peacetopia, taken from the city’s security cameras. They are labeled:
- y = 0: There is no bird on the image
- y = 1: There is a bird on the image<br>
Your goal is to build an algorithm able to classify new images taken by security cameras from Peacetopia.<br>
There are a lot of decisions to make:
- What is the evaluation metric?
- How do you structure your data into train/dev/test sets?<br>
**Metric of success**<br>
The City Council tells you the following that they want an algorithm that
1. Has high accuracy.
2. Runs quickly and takes only a short time to classify a new image.
3. Can fit in a small amount of memory, so that it can run in a small processor that the city will attach to many different security cameras.
You meet with them and ask for just one evaluation metric. True/False?<br>
- [ ] False
- [x] True

> Yes. The goal is to have one metric that focuses the development effort and increases iteration velocity.

**Question 2**<br>
The city asks for your help in further defining the criteria for accuracy, runtime, and memory. How would you suggest they identify the criteria?
- [ ] Suggest to them that they focus on whichever criterion is important and then eliminate the other two. 
- [x] Suggest to them that they define which criterion is most important. Then, set thresholds for the other two. 
- [ ] Suggest that they purchase more infrastructure to ensure the model runs quickly and accurately.

> Yes. The thresholds provide a way to evaluate models head to head.

**Question 3**<br>
Which of the following best answers why it is important to identify optimizing and satisficing metrics?
- [ ] Knowing the metrics provides input for efficient project planning. 
- [ ] It isn't. All metrics must be met for the model to be acceptable. 
- [x] Identifying the metric types sets thresholds for satisficing metrics. This provides explicit evaluation criteria. 
- [ ] Identifying the optimizing metric informs the team which models they should try first.

> Yes. Thresholds are essential for evaluation of key use case constraints.

**Question 4**<br>
**Structuring your data**<br>
Before implementing your algorithm, you need to split your data into train/dev/test sets. Which of these do you think is the best choice?
- [ ] ![image](https://github.com/user-attachments/assets/1e484e5c-7a54-4acb-9bb4-f2f9ab9378a3)
- [x] ![image](https://github.com/user-attachments/assets/c63151cf-3ab7-44e0-8b96-590190c5be30)
- [ ] ![image](https://github.com/user-attachments/assets/e1b3bfe7-b233-4203-a211-33c68dae25fb)
- [ ] ![image](https://github.com/user-attachments/assets/bab3b0a3-18a1-4029-9681-070db73c1137)

**Question 5**<br>
Now that you’ve set up your train/dev/test sets, the City Council comes across another 1,000,000 images from social media and offers them to you. These images are different from the distribution of images the City Council had originally given you, but you think it could help your algorithm. You should add the citizens’ data to the training set. True/False?
- [x] True
- [ ] False

> Yes. This will cause the training and dev/test set distributions to become different, however as long as dev/test distributions are the same you are aiming at the same target.

**Question 6**<br>
One member of the City Council knows a little about machine learning, and thinks you should add the 1,000,000 citizens’ data images to the test set. You object because:
- [x] The test set no longer reflects the distribution of data (security cameras) you most care about. 
- [ ] A bigger test set will slow down the speed of iterating because of the computational expense of evaluating models on the test set. 
- [x] This would cause the dev and test set distributions to become different. This is a bad idea because you're not aiming where you want to hit. 
- [ ] The 1,000,000 citizens' data images do not have a consistent x-->y mapping as the rest of the data.

**Question 7**<br>
You train a system, and the train/dev set errors are 3.5% and 4.0% respectively. You decide to try regularization to close the train/dev accuracy gap. Do you agree?
- [ ] Yes, because this shows your bias is higher than your variance. 
- [ ] No, because this shows your variance is higher than your bias. 
- [x] No, because you do not know what the human performance level is. 
- [ ] Yes, because having a 4.0% training error shows you have a high bias.

> Yes. You need to know what the human performance level is to estimate avoidable bias.

**Question 8**<br>
You want to define what human-level performance is to the city council. Which of the following is the best answer?
- [x] The performance of their best ornithologist (0.3%). 
- [ ] The average of all the numbers above (0.66%). 
- [ ] The average of regular citizens of Peacetopia (1.2%). 
- [ ] The average performance of all their ornithologists (0.5%).

> Yes. The best human performance is closest to Bayes' error.

**Question 9**<br>
A learning algorithm’s performance can be better than human-level performance but it can never be better than Bayes error. True/False?
- [x] True
- [ ] False

> Yes. By definition, human level error is worse than Bayes error.

**Question 10**<br>
Which of the following best expresses how to evaluate the next steps in your project when your results for human-level performance, train, and dev set error are 0.1%, 2.0%, and 2.1% respectively?
- [ ] Evaluate the test set to determine the magnitude of the variance. 
- [ ] Port the code to the target devices to evaluate if your model meets or exceeds the satisficing metrics. 
- [ ] Keep tuning until the train set accuracy is equal to human-level performance because it is the optimizing metric. 
- [x] Based on differences between the three levels of performance, prioritize actions to decrease bias and iterate.

> Yes. Always choose the area with the biggest opportunity for improvement.

**Question 11**<br>
You’ve now also run your model on the test set and find that it is a 7.0% error compared to a 2.1% error for the dev set. What should you do? (Choose all that apply)
- [ ] Try decreasing regularization for better generalization with the dev set. 
- [ ] Get a bigger test set to increase its accuracy. 
- [x] Increase the size of the dev set. 
- [x] Try increasing regularization to reduce overfitting to the dev set.

> Yes. The dev set performance versus the test set indicates it is overfitting.

**Question 12**<br>
After working on this project for a year, you finally achieve: <br>
![image](https://github.com/user-attachments/assets/5f8c5ddb-76d6-40eb-aef4-0f2826aeba52)<br>
What can you conclude? (Check all that apply.)
- [x] It is now harder to measure avoidable bias, thus progress will be slower going forward. 
- [ ] With only 0.05% further progress to make, you should quickly be able to close the remaining gap to 0% 
- [ ] This is a statistical anomaly (or must be the result of statistical noise) since it should not be possible to surpass human-level performance. 
- [x] If the test set is big enough for the 0.05% error estimate to be accurate, this implies Bayes error is ≤ 0.05

**Question 13**<br>
It turns out Peacetopia has hired one of your competitors to build a system as well. You and your competitor both deliver systems with about the same running time and memory size. However, your system has higher accuracy! Still, when Peacetopia tries out both systems, they conclude they like your competitor’s system better because, even though you have higher overall accuracy, you have more false negatives (failing to raise an alarm when a bird is in the air). What should you do?
- [ ] Pick false negative rate as the new metric, and use this new metric to drive all further development. 
- [ ] Apply regularization to minimize the false negative rate. 
- [x] Brainstorm with your team to refine the optimizing metric to include false negatives as they further develop the model. 
- [ ] Ask your team to take into account both accuracy and false negative rate during development.

> Yes. The target has shifted so an updated metric is required.

**Question 14**<br>
You’ve handily beaten your competitor, and your system is now deployed in Peacetopia and is protecting the citizens from birds! But over the last few months, a new species of bird has been slowly migrating into the area, so the performance of your system slowly degrades because your data is being tested on a new type of data.<br>
![image](https://github.com/user-attachments/assets/dafdd911-856a-4aca-a733-f93571f70c4a)<br>
You have only 1,000 images of the new species of bird. The city expects a better system from you within the next 3 months. Which of these should you do first?
- [ ] Try data augmentation/data synthesis to get more images of the new type of bird. 
- [ ] Add the 1,000 images into your dataset and reshuffle into a new train/dev/test split. 
- [ ] Put the 1,000 images into the training set so as to try to do better on these birds. 
- [x] Use the data you have to define a new evaluation metric (using a new dev/test set) taking into account the new species, and use that to drive further progress for your team.

**Question 15**<br>
The City Council thinks that having more Cats in the city would help scare off birds. They are so happy with your work on the Bird detector that they also hire you to build a Cat detector. (Wow Cat detectors are just incredibly useful, aren’t they?) Because of years of working on Cat detectors, you have such a huge dataset of 100,000,000 cat images that training on this data takes about two weeks. Which of the statements do you agree with? (Check all that agree.)
- [x] If 100,000,000 examples is enough to build a good enough Cat detector, you might be better off training with just 10,000,000 examples to gain a 10x improvement in how quickly you can run experiments, even if each model performs a bit worse because it's trained on less data. 
- [x] Buying faster computers could speed up your teams' iteration speed and thus your team's productivity. 
- [ ] Having built a good Bird detector, you should be able to take the same model and hyperparameters and just apply it to the Cat dataset, so there is no need to iterate. 
- [x] Needing two weeks to train will limit the speed at which you can iterate.
