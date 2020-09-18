## Identifying Smoking Environments From Images of Daily Life With Deep Learning

### Introduction

According to the CDC, cigarette-smoking leads to 500,000 U.S. deaths each year. Long-term smoking can result in negative health consequences, including cancer, stroke, lung disease, COPD, immune diseases, and so much more. Unfortunately, less than 20% of individuals who attempt to quit cigarette smoking achieve abstinence past 6 months. Research has shown that daily environments can actually work against smokers in their attempt to quit. There are some environments that can provoke the craving of cigarettes and smoking behavior. Continued exposure to these environments could lead to a relapse. This article discusses the applications of deep learning, specifically convolutional neural networks, in systematically analzying daily environments and predicting the probability of whether the environment represents a smoking or non-smoking environment. Ultimately, the model could be used to determine what environmental factors contributed to relapse in a smoker's behavior, and it's helpful information to know what places to avoid!

### Method

In this study, 106 participants were recruited from Durham, North Caroline and 63 from Pittsburgh, Pennyslvania. Participants took up to 4 daily photographs of non-smoking environments and 4 photographs of smoking environments. Images were taken with a digital camera. Later, participants viewed different pictures and were asked to report the smoking craving they felt and associated with the image. 

### Classification Model

A convolutional neural network was used to ultimately classify images as smoking or non-smoking environemnts. The final classifier in this study had three distinct portions. First, it contained a pretrained image classification network that provides information about image content and to recognize images or locations like patios, libraries, trash cans, chairs, etc. The second portion had infromation to relate the presence or absence of these objects (logit scores) to the probability that the image depicts a smoking or non-smoking location. This second portion has a logistic regression model that is trained on the current dataset. Together, these two constitute a single model that predicts whether an environment is smoking or non-smoking. The last layer in the model is softmax(). Essentially, this layer will take in an input of score values and "squash" them between 0-1. 

To evaluate performance, three validation schemes were used:

1. Model was developed and trained on Durham, NC data and then applied to Pittsburgh, PA
2. Model was developed and trained on Pittsburgh, PA data and then applied to Durham, NC
3. Model was developed and validated with all images jointly

Nested cross-validation was used to avoid bias error. This means that the participants were separated into 10 groups (folds). Then, for each group, the model was trained on images not from that group, and evaluated on images from that group. There was also manual classification by experts. Images from 25 randomly selected participants were sent to experts who were instructed to classify each image as "yes" or "no" depending on the following question: " Would you warn a smoker that this is an environment in which they might smoke or be tempted to smoke?" 

## Results

The mean AUC (Area under curve) across all folds was .840. AUC is just a measure of how well the model performed. A perfect classifier would have an AUC of 1.0. If the classifer was random in its guesses, the AUC would be about .5. The manual validation method had interesting results, with expert A outperforming the Pittsburgh-trained classifier. In general, classifier-predicted smoking probability for the 8 standard environments was correlated with median craving reported for that image by the study participants. 

![Screen Shot 2020-09-17 at 11 18 46 PM](https://user-images.githubusercontent.com/60228374/93551556-2e65d100-f93c-11ea-91ee-c56069982fb6.png)

The above image shows the comparison between self-reported craving scores assigned by the smokers, and the classifer probability score of an environment as a smoking or non-smoking location. The classifer recognized "patio" and "moving van" as the images/objects most strongly to influence cigarette craving, whereas "library", "grocery store", and "photocopier" were not associated with a cigarette craving. 

![Screen Shot 2020-09-17 at 11 21 44 PM](https://user-images.githubusercontent.com/60228374/93551739-9fa58400-f93c-11ea-9479-74e3f5c74143.png)

![Screen Shot 2020-09-17 at 11 23 09 PM](https://user-images.githubusercontent.com/60228374/93551819-ccf23200-f93c-11ea-9ff9-abe4964c4262.png)

The above plot is a 2-dimensional representation of all the images, generated using t-SNE. t-SNE is a dimensionality-reduction algorithm that can be used to explore highly dimensional data. The final model achieved accuracy (76.5%) significantly better than chance and comparable with human experts.

## Discussion

Ultimately, this study revealed that specific environmental features are associated with tobacco use. Oftentimes, in clinal practice, smokers are encouraged to identify situations and places from their everyday lives that trigger their craving and to avoid such things. However, this can be a difficult task, and with improvement, this model could be implemented to aid in the process. The study mentions their hope for the future, which includes applying their approach to predict smoking risk in real time. This would happen through the use of Just-in-time adaptive intervention (JITAI), where mobile devices/wearable cameras can take images and mobile devices could process the image in real-time and interact with the user through prompts or alerts. The researchers would also like to experiment with personalization to the user.

## Agent Based modelling applications

This study proves how helpful agent based models can be in assessing tobacco risk. Several population dynamic models have been used to simulate the dynamics of smoking and smoking-attributed deaths in a state or nation and the effects of policies on those outcomes. Ultimately, these models are of the utmost importance for policy-making decisions These models can help simulate the effect some policies would have on the population. The study described here really analyzed the interaction between humans and their environment, but it also showcases the need for models to analyze human to human interactions. For example, teenagers who see their older relatives smoke may be more at risk, and have different beliefs than others of how tobacco shapes health. Additonally, peer pressure is another component. Capturing social intereactions can be difficult. 
