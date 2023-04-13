# Workout - Classifier

This code represents a website where a pre-trained computer vision model is utilized to classify exercises in real-time using the camera feed of the user's device. The model is built with the [InceptionResNetV2](https://keras.io/api/applications/inceptionresnetv2/) architecture and trained on the [Workout/Exercise Images](https://www.kaggle.com/datasets/hasyimabdillah/workoutexercises-images) from Kaggle. The pre-trained model is exported to a .json file and can be used in the browser via TensorFlow.js.

## How it works

The user can select their device's camera and a canvas will show up with the camera feed. The user can perform exercises in front of the camera, and the application will use the pre-trained model to classify the exercise in real-time. The classification result will be displayed on the page.

## Getting Started

### Prerequisites

* A modern web browser with webcam support (e.g. Google Chrome, Mozilla Firefox)
* The pre-trained model file (.json) and the TensorFlow.js files

### Installation

* Clone or download this repository.
* Place the pre-trained model files (.h5) and the TensorFlow.js files in the root folder of the project.
* Open the index.html file in your web browser.

## Usage

* Open the index.html file in your web browser.
* Allow the application to access your device's camera.
* Perform exercises in front of the camera.
* The classification result will be displayed on the page.

### Starting a server in the folder

This project uses a Tensorflow.js model, which requires access through http/https. You can use any server for that, but here is a way to do it:

* Download Python on your computer
* Open a command prompt or terminal
* Navigate to the folder where you downloaded the repository
* Run the command python -m http.server 8000
* Open a browser and go to http://localhost:8000

### Using it on a mobile device

If you want to open it on your mobile device, you cannot just use the local IP address of your computer and the port, because HTTPS is required to use the camera. You can create an HTTPS tunnel by following these steps:

* Download ngrok on your computer and unzip it
* Open a command prompt or terminal
* Navigate to the folder where you downloaded ngrok
* Run the command ngrok http 8000
* It is important to have both active: the python server and the ngrok tunnel
* An HTTPS link will appear on the command prompt. You can access it with your mobile device, even if you are not on the local network.
* The tunnel expires after 2 hours, but you can restart ngrok in that case
* Open a browser on your mobile device and go to the indicated HTTPS link.

## Model Training

The model was trained using Python and TensorFlow in Google Colab, and the Colab notebook is also included in the repository.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/sonosergi/Workout-Classifier/blob/main/LICENSE) file for details. 
