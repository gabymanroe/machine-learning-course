Question 1
This example is adapted from a real production application, but with details disguised to protect confidentiality.
![image](https://github.com/user-attachments/assets/226e4699-a67f-4e09-80a1-f777e0ef7d4e)
You are a famous researcher in the City of Peacetopia. The people of Peacetopia have a common characteristic: they are afraid of birds. To save them, you have to build an algorithm that will detect any bird flying over Peacetopia and alert the population.
The City Council gives you a dataset of 10,000,000 images of the sky above Peacetopia, taken from the city’s security cameras. They are labeled:
- y = 0: There is no bird on the image
- y = 1: There is a bird on the image
Your goal is to build an algorithm able to classify new images taken by security cameras from Peacetopia.
There are a lot of decisions to make:
What is the evaluation metric?
How do you structure your data into train/dev/test sets?
Metric of success
The City Council tells you the following that they want an algorithm that
1. Has high accuracy.
2. Runs quickly and takes only a short time to classify a new image.
3. Can fit in a small amount of memory, so that it can run in a small processor that the city will attach to many different security cameras.
You meet with them and ask for just one evaluation metric. True/False?
False
True

Question 2
The city asks for your help in further defining the criteria for accuracy, runtime, and memory. How would you suggest they identify the criteria?
