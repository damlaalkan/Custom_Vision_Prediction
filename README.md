# Custom_Vision_Prediction

Azure Custom Vision is a cognitive service that lets you build, deploy, and improve your own image classifiers. An image classifier is an AI service that applies labels (which represent classes) to images, according to their visual characteristics. Unlike the Computer Vision service, Custom Vision allows you to determine the labels to apply.
The Custom Vision service uses a machine learning algorithm to apply labels to images. You, the developer, must submit groups of images that feature and lack the characteristics in question. You label the images yourself at the time of submission. Then the algorithm trains to this data and calculates its own accuracy by testing itself on those same images. Once the algorithm is trained, you can test, retrain, and eventually use it to classify new images according to the needs of your app. You can also export the model itself for offline use.
Custom Vision functionality can be divided into two features. Image classification applies one or more labels to an image. Object detection is similar, but it also returns the coordinates in the image where the applied label(s) can be found.


Upload and tag images, train them and test quickly. You can see the test results in Prediction tab. In Performance tab To submit images to the Prediction API, you will first need to publish your iteration for prediction, which can be done by selecting Publish and specifying a name for the published iteration. This will make your model accessible to the Prediction API of your Custom Vision Azure resource.
Once your model has been successfully published, you'll see a "Published" label appear next to your iteration in the left-hand sidebar, and its name will appear in the description of the iteration.Once your model has been published, you can retrieve the required information by selecting Prediction URL. This will open up a dialog with information for using the Prediction API, including the Prediction URL and Prediction-Key.

Change the following information:

Set the namespace field to the name of your project.

Replace the placeholder <Your prediction key> with the key value you retrieved earlier.

Replace the placeholder <Your prediction URL> with the URL you retrieved earlier.


            client.DefaultRequestHeaders.Add("Prediction-Key", "<Your prediction key>");
            string url = "<Your prediction URL>";
