MNIST Neural Network (Java)

This project shows a very simple neural network in Java that works on the famous MNIST digit dataset (handwritten numbers 0–9).
The main goal here is to see how data flows forward through a network, not to actually train it.

What it does

Reads the Kaggle Digit Recognizer dataset (train.csv).

Scales down the pixel values so they’re between 0 and 1.

Passes the images through a tiny neural network:

Input → Hidden layer (ReLU) → Output layer (Softmax)

Calculates:

Loss (how far off the predictions are)

Accuracy (how many guesses are right)

Runs for a few “epochs” (loops through the dataset).

What it does not do

This is forward pass only:

It does not learn or adjust weights (no backpropagation).

Accuracy will stay close to random guessing (~10%).

It’s just a demo of the mechanics, not a real training model.

Files
neuralnetwork.java    # Main program
hidden_layer.java     # Layer with weights & biases
relu.java             # ReLU activation function
softmax.java          # Softmax activation
lossfunction.java     # Cross-entropy loss

How to run

Go to Kaggle and download the dataset: Digit Recognizer.

Put train.csv in the same folder as the Java files.

Open a terminal in that folder and run:

javac neuralnetwork.java
java neuralnetwork


You’ll see output like:

Epoch 1 | Loss: 2.3015 | Acc: 0.127
Epoch 2 | Loss: 2.3015 | Acc: 0.127
...

Next Steps (if you want to go further)

Add backpropagation so the network actually learns.

Try different numbers of hidden units or layers.

Split the data into training and testing.

Show predictions and errors visually.
