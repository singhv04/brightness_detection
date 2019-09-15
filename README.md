# brightness_detection

* Note: the error while training "filenotfound" occured as i moved the folder train and val to other directory during the training for uploading only necessary files on github.

* Requirements

  * apt-get install python3-pip
  * pip3 install torch
  * pip3 install torchvision
  * pip3 install opencv-python
  * pip3 install matplotlib
  * pip3 install numpy
  * pip3 install Pillow

  * JPEGImages folder (from Imagenet dataset): Provided

* Dataset preperation:
  * Downloaded the Imagenet dataset
  * Took JPEGImages folder in current directory
  * Everything else is generated using this python program
  * As i needed to prepare the dataset for brightness detection so ran simple image analysis 
  * Tested different method, they all seem to returns a close value, but not exactly the same as the others. Almost all methods run about the same speed except where we calculated "perceived brightness" of pixels, then return average which is much slower depending on the image size.

* Visualized the color-distribution after normalizing the perceived brightness value between 0-10 as we needed 10 classes
   * Saved the images according in different folder named as their corresponding labels

* Model building
  * Used pytorch for it.
  * Used transfer learning where i basically took pretrained resnet18 and removed the last layer and trained it again on my dataset.
  * Applied data augmentation for further increasing the data

* Training
  * Trained on Intel® Core™ i5 with default Intel® HD Graphics 520 graphic card.
  * Due to hardware limitation its trained just for 5 epochs  
  * Can be trained on colab for much better results

* Testing
  * Tested the model on images saved in validation folder

* Visualizing some results
  * Visualized the performance on random validation images
