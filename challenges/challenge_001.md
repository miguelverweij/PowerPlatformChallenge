## Challenge 001
For the first challenge we are building an AI model which will detect if you are wearing a facemask. We will implement the AI model in an app.

### Discussion board
[DISCUSSION FOR CHALLENGE 001](https://github.com/miguelverweij/PowerPlatformChallenge/discussions/4)

## Challenge instructions
The Power Platform enables everyone to streamline whatever process they are dealing with. Ideally you want to automate the whole process. With power Automate and Power Apps you can do a huge amount of automation, but some processes need some cognitive skills. Traditionally this would mean we need human input, but nowadays we can utilize the power of AI.
The Power Platform comes with AI Builder which enables you to infuse AI in your solution. Simply put it is the power of Azure Cognitive Services in a low-code form.

AI Builder comes with some pre-built AI models that you can directly use, but there is not a pre-built model that can check if you are wearing a face mask. If you are interested in tose, Microsoft created some [AI BUIDLER HANDS-ON LABS](https://go.microsoft.com/fwlink/?linkid=2103171) that you can check out. But for this challenge we need tto build a model ourselves.

Developing an AI model means training and testing it. This used to be a time consuming task which required quite some developer skills. But in the low-code heaven it is as easy as creating a TikTok video (I think...). There is a seperate app available called Lobe that helps you build the model. Once you have created the model you can export it to your Power Platform environment. That is exactly what we are going to do. Follow the steps below to build the AI model.

1. [DOWNLOAD](https://www.lobe.ai/) Lobe from their website.
2. Open the app once downloaded.
3. Create New Project.
4. Name the project Face Mask.
5. Click Import.
6. Select Camera.
7. Name the label No Mask.
8. Take some selfies (5 minimum) while not wearing a face mask. PRO TIP: Keep the button pressed for bursting and move your head. The more images from multiple angles, the better the prediction will be. ![Lobe Training](/assets/LobeTraining.gif "Lobe Training")
9. Select the Label and type Mask. A new label will be made.
10. Grab a face mask and put it on.
11. Again, take some selfies. This time you can skip the duck-face.
12. Notice that while adding pictures Lobe starts training the model. Once it's done training you have created an AI model.

It wasn't that hard right? You could now export the model to your Power Platform environment and start using it. But before we do that, we will test is it is doing what we want it to do. In Lobe, select Use. See the live prediction from your model. A cool feature in Lobe is that you can make adjustments to your model while testing it. If you see some errors you can correct it. Lobe will instantly train the model again with your new input. Making some adjustments is what we are going to do.

1.  Put on your mask. Make sure it is not covering your nose.
2.  See the prediction from your model. It is probably thinking you are wearing a face mask. Click on the prediction and select the label No Mask.
3.  Repeat this a few times and let Lobe train the model again.
4.  Now cover your nose again with the face mask. If there is a wrong prediction, correct it.
5.  Switch between covering and not covering your nose and make changes until the model is good enough.

That's it! You just created an AI model that cannot only detect if someone is wearing a face mask, but also predict if it is worn properly. Now let's make sure we can use this model in an app.

1.  on the Use tab in Lobe, select Export.
2.  From all the options, select Power Platform.
3.  Sign in with your Microsoft Developer Program account.
4.  Name your model Face Mask and select the default environment.
5.  Now you can export your model. It is recommended to optimize your model. This will take less than a minute.
6.  Once the model is exported, you can view your model.
7.  AI Builder is a premium feature. Start a trial for AI Builder.

You are now ready to use your model in a flow or app. Feel free to build whatever you want with it. If you have a cool suggestion on how this model can be used, or got inspired to build another model and use it for some specific scenario, please share it in the [DISCUSSION](https://github.com/miguelverweij/PowerPlatformChallenge/discussions/4) for this challenge. For those who want to know how to build an AI Builder enables app, follow the steps below.

1. Create a new Canvas app
2. On the Data tab, click add data and search for Face Mask in the AI Builder section
3. Add a camera control
4. Set the stream rate to 100
5. Add a button
6. Put the following function in the OnSelect. 
``` Set(varFaceMaskOutput, 'Face Mask'.Predict(Camera1.Stream).Prediction)```
7.  Add a label with varFaceMaskOutput as text
8.  Select the Button

Your app will now create an image and send it to the server to be analyzed. The label will show you the prediction. You can obviously make functionality in your app depending on the prediction. The technology is there. It is up to your creativity to implement it usefully.

## Example solution
You can [DOWNLOAD](/assets/Challenge001_1_0_0_0.zip) my example solution.