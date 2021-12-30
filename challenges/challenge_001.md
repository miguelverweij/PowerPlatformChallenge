## Challenge 001
For the first challenge we are building an AI model which will detect if you are wearing a facemask. We will implement the AI model in an app.

### Discussion board
[Discussion for Challenge 001](https://github.com/miguelverweij/PowerPlatformChallenge/discussions/4)

## Challenge instructions
The Power Platform enables everyone to streamline whatever process they are dealing with. Ideally you want to automate the whole process. With power Automate and Power Apps you can do a huge amount of automation, but some processes need some cognitive skills. Traditionally this would mean we need human input, but nowadays we can utilize the power of AI.
The Power Platform comes with AI Builder which enables you to infuse AI in your solution. Simply put it is the power of Azure Cognitive Services in a low-code form.

AI Builder comes with some pre-built AI models that you can directly use, but there is not a pre-built model that can check if you are wearing a face mask. If you are interested in tose, Microsoft created some [AI Builder hands-on labs](https://go.microsoft.com/fwlink/?linkid=2103171) that you can check out. But for this challenge we need tto build a model ourselves.

Developing an AI model means training and testing it. This used to be a time consuming task which required quite some developer skills. But in the low-code heaven it is as easy as creating a TikTok video (I think...). There is a seperate app available called Lobe that helps you build the model. Once you have created the model you can export it to your Power Platform environment. That is exactly what we are going to do. Follow the steps below to build the AI model.

1. [DOWNLOAD](https://www.lobe.ai/) Lobe from their website
2. Open the app once downloaded
3. Create New Project
4. Name the project Face Mask
5. Click Import
6. Select Camera
7. Name the label No Mask
8. Take some selfies (5 minimum) while not wearing a face mask. PRO TIP: Keep the button pressed for bursting and move your head. The more images from multiple angles, the better the prediction will be.

![Lobe Training](/assets/LobeTraining.gif "Lobe Training")
9. Select the Label and type Mask. A new label will be made.
10. Grab a face mask and put it on.
11. Again, take some selfies. This time you can skip the duck-face.
12. Notice that while adding pictures Lobe starts training the model. Once it's done training you have created an AI model. It wasn't that hard right?
13. Now that you have your model, you can start using it. You can directly export it to 
