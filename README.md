# CameraModelIdentification
#### The purpose of this project is to analyze images to identify the camera that the image was taken from. The objective is to build an algorithm that identifies which camera model captured an image by using traces intrinsically left in the image.
#### Data Link 
#### https://www.kaggle.com/c/sp-society-camera-model-identification/data
#### Data Collection/Description
##### Training images were taken with 10 different camera models, a single device per model, with 275 full images from each device for a total of 2750 images. With limited processing power i was only able to load and analyze 500. 
#### Camera Models: 
##### Sony NEX-7, Motorola Moto X, Motorola Nexus6, Motorola DROID MAXX, LG Nexus 5x, Apple iPhone 6, Apple iPhone 4s, HTC One M7, Samsung Galaxy S4, Samsung Galaxy Note 3
##### Test images were captured with the same 10 camera models, but with a second device 
##### I started off with my exploratory data analysis by looking at EXIF Offset data for each image. Below is a plot that shows the EXIF offset numbers by camera. 
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/exif_plot_1.png" alt = "This plot shows the EXIF offset numbers by camera" title="EXIF Offset Images By Camera Model" />]

##### Below is another plot of the same EXIF Offset numbers but in scatter plot format. 
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/exif_plot_2.png" alt="Scatter plot of EXIF offset numbers by camera" title="Scatter EXIF Offset Images by Camera Model." />

##### Looking at the EXIF Offset numbers did not prove very useful so i started looking at noise data for images by camera model. Below are the plots for the noise images. 
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/htc-1-m7_noise.png" alt="HTC-1-m7" title="HTC 1 M7 Noise Image" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/iPhone-4s_noise.png" alt="iPhone-4s" title="iPhone 4S Noise Image" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/iPhone-6_noise.png" alt="iPhone 6" title="iPhone 6 Noise Image" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/LG-Nexus-5x_noise.png" alt="LG Nexus 5x" title="LG Nexus 5x Noise Image" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/Motorola-Droid-Maxx_noise.png" alt="Motorola-Droid-Maxx" title="Motorola Droid Maxx Noise Image" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/Motorola-Nexus-6_noise.png" alt="Motorola Nexus 6" title="Motorola Nexus 6 Noise Image" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/Motorola-X_noise.png" alt="Motorola X" title="Motorola X Noise Image" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/Samsung-Galaxy-Note3_noise.png" alt="Samsung Galaxy Note 3" title="Samsung Galaxy Note3 Noise Image" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/Samsung-Galaxy-S4_noise.png" alt="Samsung Galaxy S4" title="Samsung Galaxy S4 Noise Image" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/Sony-NEX-7_noise.png" alt="Sony NEX 7" title="Sony NEX 7 Noise Image" />


##### Ultimately i ended up using RGB values to build the models. I trained 3 different models. Logistic model, KNN and Decision Tree. Below is the performance of each one of those models 

##### Below are some RGB image samples 
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/rgb_1.png" alt="RGB" title="RGB" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/rgb_3.png" alt="RGB" title="RGB" />

#### Logistic Regression Stats 
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/logistic_1.png" alt="Logistic Model" title="Logistic Model" />

<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/logistic_2.png" alt="Logistic Model" title="Logistic Model" />

## KNN Stats 

<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/Knn_1.png" alt="KNN Model" title="KNN Model" />
<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/Knn_2.png" alt="KNN Model" title="KNN Model" />

## Decision Tree 

<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/dt_1.png" alt="Decision Treee Model" title="Decision Tree Model" />

#### A comparison of the three models' accuracy scores shows that the logistic model performed the best with the decision tree model second in line 

<img src="https://github.com/heatherholcomb/CameraModelIdentification/blob/master/ModelComparison.png" alt="Model Comparison" title="Model Comparison" />

## References 

#### https://machinelearningmastery.com/how-to-load-large-datasets-from-directories-for-deep-learning-with-keras/
#### https://www.geeksforgeeks.org/iterate-over-a-list-in-python/
#### ://towardsdatascience.com/image-data-analysis-using-python-edddfdf128f4
#### https://docs.opencv.org/3.4/dc/dbb/tutorial_py_calibration.html
#### https://medium.com/analytics-vidhya/camera-calibration-with-opencv-f324679c6eb7
#### https://github.com/RenatoBMLR/Camera-Model-Identification/blob/master/camera-model-identification.ipynb
#### https://www.kaggle.com/c/sp-society-camera-model-identification/data
