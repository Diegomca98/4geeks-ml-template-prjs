# Image Classifier Project Tutorial

* Understanding a new dataset.
* Model the data using an ANN.
* Analyze the results and optimize the model.

## Image Classification System
> The dataset is composed of dog and cat photos provided as a subset of photos from a much larger 3 million manually annotated photos. This data was obtained through a collaboration between Petfinder.com and Microsoft.
> 
> The data set was originally used as a CAPTCHA, i.e., a task that a human is believed to find trivial, but that a machine cannot solve, which is used on websites to distinguish between human users and bots. The task was named "Asirra". When "Asirra" was introduced, it was mentioned "that user studies indicate that humans can solve it 99.6% of the time in less than 30 seconds." Barring a breakthrough in computer vision, we expect that computers will have no more than a 1/54,000 chance of solving it.
> 
> At the time the competition was published, the state-of-the-art result was achieved with an SVM and was described in a 2007 paper with the title "Machine Learning Attacks against Asirra's CAPTCHA" (PDF) that achieved 80% classification accuracy. It was this paper that showed that the task was no longer a suitable task for a CAPTCHA shortly after the task was proposed.
>

### Step 1: Loading the dataset
The dataset is located in Kaggle and you will need to access it to download it. You can find the competition [here](https://www.kaggle.com/c/dogs-vs-cats/data).

Download the datatset folder and unzip the files. You will now have a folder called `train` containing 25,000 image files (.jpg format) of dogs and cats. The pictures are labeled by their file name, with the word `dog` or `cat`.

### Step 2: Visualize the input information
The first step when faced with a picture classification problem is to get as much information as possible through the pictures. Therefore, load and print the first nine pictures of dogs in a single figure. Repeat the same for cats. You can see that the pictures are in color and have different shapes and sizes.

This variety of sizes and formats must be sorted out before entering the model. Make sure they all have a fixed size of `200x200` pixels.

As you can see, there are a lot of images, make sure you follow the following rules:

1. **If you have more than 12 gigabytes of RAM**, use the Keras image processing API to load the 25,000 photos into the training dataset and reshape them to 200×200 pixel square photos. The label must also be determined for each photo based on the file names. A tuple of photos and labels should be saved.
2. **If you have no more than 12 gigabytes of RAM**, load the images progressively using the Keras `ImageDataGenerator` class and the `flow_from_directory()` function. This will be slower to run but will run on less capable hardware. This function prefers the data to be split into separate `train/` and `test/` directories, and under each directory to have a subdirectory for each class.

Once you have all the images processed, create an `ImageDataGenerator` object for training and test data. Then pass the folder that has training data to the `trdata` object and, similarly, pass the folder that has test data to the `tsdata` object. In this way, the images will be automatically labeled and everything will be ready to enter the network.

### Step 3: Build an ANN
Any classifier that fits this problem will have to be robust because some images show the cat or dog in a corner or perhaps 2 cats or dogs in the same picture. If you have been able to research some of the winner implementations of other competitions also related to images, you will see that `VGG16` is a CNN architecture used to win the *Kaggle ILSVR (Imagenet)* competition in 2014. It is considered one of the best performing vision model architectures to date.

It uses the following test architecture:

```
model = Sequential()
model.add(Conv2D(input_shape = (224,224,3), filters = 64, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(Conv2D(filters = 64,kernel_size = (3,3),padding = "same", activation = "relu"))
model.add(MaxPool2D(pool_size = (2,2),strides = (2,2)))
model.add(Conv2D(filters = 128, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(Conv2D(filters = 128, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(MaxPool2D(pool_size = (2,2),strides = (2,2)))
model.add(Conv2D(filters = 256, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(Conv2D(filters = 256, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(Conv2D(filters = 256, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(MaxPool2D(pool_size = (2,2),strides = (2,2)))
model.add(Conv2D(filters = 512, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(Conv2D(filters = 512, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(Conv2D(filters = 512, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(MaxPool2D(pool_size = (2,2),strides = (2,2)))
model.add(Conv2D(filters = 512, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(Conv2D(filters = 512, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(Conv2D(filters = 512, kernel_size = (3,3), padding = "same", activation = "relu"))
model.add(MaxPool2D(pool_size = (2,2),strides = (2,2)))
model.add(Flatten())
model.add(Dense(units = 4096,activation = "relu"))
model.add(Dense(units = 4096,activation = "relu"))
model.add(Dense(units = 2, activation = "softmax"))
```

The above code applies convolutions to the data (`Conv2D` and `MaxPool2D` layers) and then applies dense layers (`Dense` layers) for processing the numerical values obtained after the convolutions.

Then add the remaining elements to form the model, train it and measure its performance.

### Step 4: Optimize the above model
Import the `ModelCheckpoint` and `EarlyStopping` method from Keras. Create an object of both and pass them as callback functions to `fit_generator`.

Load the best model from the above and use the test set to make predictions.

### Step 5: Save the model
Store the model in the corresponding folder.