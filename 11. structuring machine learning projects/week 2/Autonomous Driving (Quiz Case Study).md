**Question 1**<br>
To help you practice strategies for machine learning, this week we’ll present another scenario and ask how you would act. We think this “simulator” of working in a machine learning project will give an idea of what leading a machine learning project could be like!<br>
You are employed by a startup building self-driving cars. You are in charge of detecting road signs (stop sign, pedestrian crossing sign, construction ahead sign) and traffic signals (red and green lights) in images. The goal is to recognize which of these objects appear in each image. As an example, this image contains a pedestrian crossing sign and red traffic lights.<br>
![image](https://github.com/user-attachments/assets/a3f6fd70-f13a-4dcd-8c92-7de1f78c3501)<br>
Your 100,000 labeled images are taken using the front-facing camera of your car. This is also the distribution of data you care most about doing well on. You think you might be able to get a much larger dataset off the internet, which could be helpful for training even if the distribution of internet data is not the same.<br>
You are getting started with this project. What is the first thing you do? Assume each of the steps below would take about an equal amount of time (a few days).
- [x] Train a basic model and do error analysis. 
- [ ] Invest a few days in thinking on potential difficulties, and then some more days brainstorming about possible solutions, before training any model. 
- [ ] Spend some time searching the internet for the data most similar to the conditions you expect on production. 
- [ ] Spend a few days collecting more data using the front-facing camera of your car, to better understand how much data per unit time you can collect.

> Applied ML is highly iterative. Having a basic model to do an error analysis can point you in the most promising directions with a lot of certainties.

**Question 2**<br>
Your goal is to detect road signs (stop sign, pedestrian crossing sign, construction ahead sign) and traffic signals (red and green lights) in images. The goal is to recognize which of these objects appear in each image. You plan to use a deep neural network with ReLU units in the hidden layers.  For the output layer, which of the following gives you the most appropriate activation function?
- [ ] Linear
- [ ] ReLU
- [x] Sigmoid
- [ ] Softmax

> This works well since the output would be valued between 0 and 1 which represents the probability that one of the possibilities is present in an image.

**Question 3**<br>
When trying to determine what strategy to implement to improve the performance of a model, we manually check all images of the training set where the algorithm was successful. True/False?
- [ ] True
- [x] False

> This set should be too large to manually check all the images. It is better to focus on the images that the algorithm got wrong from the dev set. Also, choose a large enough subset that we can manually check.

**Question 4**<br>
After working on the data for several weeks, your team ends up with the following data:
- 100,000 labeled images taken using the front-facing camera of your car.
- 900,000 labeled images of roads downloaded from the internet.
- Each image’s labels precisely indicate the presence of any specific road signs and traffic signals or combinations of them. For example, ![image](https://github.com/user-attachments/assets/4efab90e-daa1-4f91-a4a5-d2f6757b43a3) means the image contains a stop sign and a red traffic light.<br>
When using a non fully labeled image such as ![image](https://github.com/user-attachments/assets/5c231c72-f569-4b4e-8a55-19f2307c0712), which of the following strategies is most appropriate to calculate the loss function to train as a multi-task learning problem?
- [ ] It is not possible to use non fully labeled images if we train as a multi-task learning problem.
- [ ] Make the missing entries equal to 0.
- [ ] Make the missing entries equal to 1.
- [x] Calculate the loss as ![image](https://github.com/user-attachments/assets/dda289b5-756c-4258-8c4b-5102c251e68a) where the sum goes over all the know components of y^(i).

> We can't use the components of the labels that are missing but we can use the ones we have to train the model.

**Question 5**<br>
The distribution of data you care about contains images from your car’s front-facing camera, which comes from a different distribution than the images you were able to find and download off the internet. Which of the following are true about the train/dev/test split?
- [x] The dev and test set must come from the front-facing camera. 
> This is the distribution we care about most, thus we should use this as a target.
- [ ] The train, dev, and test must come from the same distribution.
- [x] The dev and test sets must come from the same distribution.
> This is required to aim the target where we want to be.
- [ ] The dev and test sets must contain some images from the internet.

**Question 6**<br>
Assume you’ve finally chosen the following split between the data:<br>
![image](https://github.com/user-attachments/assets/137387b4-49d3-456d-a8dd-9b4e89b63436)<br>
You also know that human-level error on the road sign and traffic signals classification task is around 0.5%. Which of the following is true?
- [ ] You have a high bias. 
- [ ] The size of the train-dev set is too high. 
- [ ] You have a large data-mismatch problem. 
- [x] You have a high variance problem.

> Since the difference between the training-dev error and the training error is high.

**Question 7**<br>
Assume you’ve finally chosen the following split between the data:<br>
![image](https://github.com/user-attachments/assets/6149df72-dd43-4397-b19d-ed6294442bb2)<br>
You also know that human-level error on the road sign and traffic signals classification task is around 0.5%. Based on the information given you conclude that the Bayes error for the dev/test distribution is probably higher than for the train distribution. True/False?
- [ ] True
- [x] False

**Question 8**<br>
You decide to focus on the dev set and check by hand what are the errors due to. Here is a table summarizing your discoveries: <br>
![image](https://github.com/user-attachments/assets/1499c7ea-d25e-4d9f-8d33-1fe3755f8d01)<br>
In this table, 4.1%, 8.0%, etc. are a fraction of the total dev set (not just examples of your algorithm mislabeled). For example, about 8.0/15.3 = 52% of your errors are due to foggy pictures.<br>
The results from this analysis implies that the team’s highest priority should be to bring more foggy pictures into the training set so as to address the 8.0% of errors in that category. True/False?<br>
Additional note: there are subtle concepts to consider with this question, and you may find arguments for why some answers are also correct or incorrect. We recommend that you spend time reading the feedback for this quiz, to understand what issues that you will want to consider when you are building your own machine learning project. 
- [ ] First start with the sources of error that are least costly to fix. 
- [ ] True because it is greater than the other error categories added together 8.0 > 4.1 + 2.2+ 1.0. 
- [x] False because it depends on how easy it is to add foggy data. If foggy data is very hard and costly to collect, it might not be worth the team's effort. 
- [ ] True because it is the largest category of errors. We should always prioritize the largest category of errors as this will make the best use of the team's time.

> You should consider the tradeoff between the data accessibility and potential improvement of your model trained on this additional data.

**Question 9**<br>
You can buy a specially designed windshield wiper that helps wipe off some of the raindrops on the front-facing camera. <br>
![image](https://github.com/user-attachments/assets/380364ce-86f7-4a9d-a11a-db25063eb5c4)<br>
Which of the following statements do you agree with? 
- [ ] 2.2% would be a reasonable estimate of the minimum amount this windshield wiper could improve performance. 
- [x] 2.2% would be a reasonable estimate of the maximum amount this windshield wiper could improve performance. 
- [ ] 2.2% would be a reasonable estimate of how much this windshield wiper could worsen performance in the worst case. 
- [ ] 2.2% would be a reasonable estimate of how much this windshield wiper will improve performance.

> You will probably not improve performance by more than 2.2% by solving the raindrops problem. If your dataset was infinitely big, 2.2% would be a perfect estimate of the improvement you can achieve by purchasing a specially designed windshield wiper that removes the raindrops.

**Question 10**<br>
You decide to use data augmentation to address foggy images. You find 1,000 pictures of fog off the internet, and “add” them to clean images to synthesize foggy days, like this:<br>
![image](https://github.com/user-attachments/assets/4d522627-408f-4de0-8ac0-b86346a66430)<br>
We can't use this data since they have a different distribution from the ones we used (internet and front-facing camera). True/False?
- [x] False
- [ ] True

> The new synthesized images are added to the training set and as long as they look realistic to the human eye this will be useful data to train the model.

**Question 11**<br>
After working further on the problem, you've decided to correct the incorrectly labeled data. Your team corrects the labels of the wrongly predicted images on the dev set.<br>  
You have to correct the labels of the test so test and dev sets have the same distribution, but you won't change the labels on the train set because most models are robust enough they don't get severely affected by the difference in distributions. True/False?
- [ ] False, the test set shouldn't be changed since we want to know how the model performs in real data. 
- [ ] False, the test set should be changed, but also the train set to keep the same distribution between the train, dev, and test sets. 
- [x] True, as pointed out, we must keep dev and test with the same distribution. And the labels at training should be fixed only in case of a systematic error.

> To successfully train a model, the dev set and test set should come from the same distribution. Also, the deep learning models are robust enough to handle a small change in distributions, but if the errors are systematic they can significantly affect the training of the model.

**Question 12**<br>
One of your colleagues at the startup is starting a project to classify road signs as stop, dangerous curve, construction ahead, dead-end, and speed limit signs. Given how specific the signs are, he has only a small dataset and hasn't been able to create a good model. You offer your help providing the trained weights (parameters) of your model to transfer knowledge.<br> 
But your colleague points out that his problem has more specific items than the ones you used to train your model. This makes the transfer of knowledge impossible. True/False
- [ ] True
- [x] False

> The model can benefit from the pre-trained model since there are many features learned by your model that can be used in the new problem.

**Question 13**<br>
One of your colleagues at the startup is starting a project to classify road signs as stop, dangerous curve, construction ahead, dead-end, and speed limit signs. He has approximately 30,000 examples of each image and 30,000 images without a sign. This case could benefit from using multi-task learning. True/False?
- [ ] False
- [x] True

> There are a lot of high-level features that all the required signs share. This is a great scenario to make use of multi-task learning.

**Question 14**<br>
To recognize red and green lights, you have been using this approach:
- **(A)** Input an image (x) to a neural network and have it directly learn a mapping to make a prediction as to whether there’s a red light and/or green light (y).<br>
A teammate proposes a different, two-step approach:
- **(B)** In this two-step approach, you would first (i) detect the traffic light in the image (if any), then (ii) determine the color of the illuminated lamp in the traffic light.<br>
Between these two, Approach B is more of an end-to-end approach because it has distinct steps for the input end and the output end. True/False? 
- [x] False
- [ ] True

> (A) is an end-to-end approach as it maps directly the input (x) to the output (y).

**Question 15**<br>
An end-to-end approach doesn't require that we hand-design useful features, it only requires a large enough model. True/False?
- [ ] False
- [x] True

> This is one of the major characteristics of deep learning models, that we don't need to hand-design the features.
