# Laser-character-recognition
I trained a neural network to recognise characters on laser chips used by Eblana Photonics. 

The idea for this project came from a real life problem we were facing in Eblana. Before sending laser chips over to customers or for laser packageing or when testing the lasers, the Ops team has to perform Visual Inspection (VI). VI is inspecting lasers images for breakage, scratches, damage and then recording the laser identifier numbers of those lasers. The Ops team faced three main challanges: 1. At times it was difficult to decifer the numbers on the lasers due to the font size or bad meal lift-off. 2. It's time consuming to record the numbers manually. 3. It's really straining for the eyes. To make a life easier for everyone I decided to create a custom Eblana laser character recognition model- like MNIST for Eblana lasers. 

For the laser chip characters we use a specific font- it is due to the fabrication process and peeling off the unnecessary layers. We use a combination of numbers and letters: 0-9 and A-Z, a-z excluding some letters like I, O. 

## Project stages:
# 1. Gathering laser images.
This was one of the most time consuming phases of the project. I had to go through many sub-folders to find laser images. Overall I gathered 80 000 images to ensure I will have a good spread of the characters and some variety. 

# 2. Extracting the characters form the laser images. 
This was a bit of a challange. The images veried in shape and sizes so I couldn't use fixed contour size. At the end I made the decision to extract all contours 
from the images, then manually siff through them and put the extracted charecters- letters and numbers into a separate folder. This part of the project can 
definitely be impoved in the future when working with new laser images.  

# 3. Resizing and converting to grey scale.
# 4. Clustering. 
I used KMeans algorithm to cluter character images.
# 5. Creating train- test set and converting them to Idx format.
# 6. Training a neural netowrk. 
I tried different models during this phase. I used convolutional neral networks with two hidden layers and two drop-out layers as I faced overfitting problem. 
# 7. Testing on real life images. 
I had to ensure that the model works on real life laser images not only on individual test characters. In short: It worked! 

## Bottom Notes 

Please note that you won't be able to run the code because of the size of the image data. However, I included some sample images just to give you an idea what I was working with. Already, I noticed places in this project that can be improved and I will be working on those impovements. There is also a secod part of this project that I'm currently working on. The second phase is to train a neural network to distinguish between good and bad lasers (as mentioned above looking for damages, scratches etc.)

      
