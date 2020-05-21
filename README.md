# Face Detection using FaceNet
Detecting faces in images is one of the hottest topics in Computer Vision. In this notebook, I will use a FaceNet model to detect and extract faces from images, and then classify them using a SVM algorithm.

The FaceNet model is a Keras model pretrained with 1M faces of celebrities, so it's a good choice for this task. The images on which we are going to apply the face detection is a small subset of 5 classes/celebrities, each one with its corresponding train and test images.

## Step-by-step
Before attempting the classification of faces, preprocessing the images is a must. In particular, this is the procedure we will follow:
- load the images from their directories.
- apply a detector (MTCNN) to obtain a bounding box around the face.
- store the faces.
- pass the faces to the FaceNet model to get the embeddings.
- store the embeddings.
- pass the embeddings to the SVM algorithm to train it.
- get predictions on a test set.

## Future work
Obviously, the FaceNet model can not be improved, at least by me, given the computational resources required. Then, a creative idea could be to add more celebrities from the original fataset.