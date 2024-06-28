# Rock-Paper-Scissors Image Classification Model

An image classification model made to identify hands in the shape of rocks, papers, or scissors.

A video showing how to run the model can be found below.

https://drive.google.com/file/d/1j3CXNB5NrmzdRlFliaCZ7FZ9et3lwBQC/view?usp=sharing

## Running the model

### 1: Ensure docker and jetson-inference are installed

sudo docker ps
cd jetson-inference

### 2: Change directories

jetson-inference/python/training/classification/data

### 3: Download the dataset

https://www.kaggle.com/datasets/wgcleveland/rock-paper-scissors/settings

### 4: Move the dataset into the current directory (jetson-inference/python/training/classification/data)

### 5: Change directories

nvidia/jetson-inference/

### 6: Ensure that memory is overcommited

echo 1 | sudo tee /proc/sys/vm/overcommit_memory

### 7: Set variables for the following command

NET=models/game_model/
DATASET=data/game_dataset/

### 8: Run Images

imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt data/game_dataset//test/paper/WIN_20240627_14_56_20_Pro.jpg output_file.jpg

 ## Sources

 https://www.kaggle.com/datasets/glushko/rock-paper-scissors-dataset
 https://github.com/alessandro-giusti/rock-paper-scissors

 



