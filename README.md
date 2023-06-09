# Project8-OpenClassrooms
Deploy a model in the cloud

## Business case
The young AgriTech start-up, named "Fruits!",
seeks to offer innovative solutions for fruit harvesting.

The company's desire is to preserve the biodiversity of the fruits
by allowing specific treatments for each species of fruit
by developing intelligent picking robots.

The start-up initially wants to make itself known to the general public by developing a mobile application that allows
users to take a picture of a fruit and get information about that fruit.

This application will help to raise awareness 
to the biodiversity of fruits and to set up a first version of the classification engine of fruit images.

In addition, the development of the mobile application will make it possible to build a first version of the necessary Big Data architecture.
## Objectives 

Develop a pipeline that
includes preprocessing and a dimension reduction step, taking into account that the volume of data will increase very soon after the delivery of this project. This mean that it is necessary to:
 - Deploy the pipeline in a Big Data environment
 - Develop scripts in Pyspark to perform distributed computing

## Main results

I created a cluster to deal with the future workload increase based on EC2 instances of AWS.

I also used the EMR service, which allows to instantiate the cluster which I could request the installation and configuration of several programs and libraries needed for the project.

Finally, I was able to run a notebook on AWS and process 12884 images. The pipeline includes:

-	image resizing
-	transfer learning with MobileNetV2 model to extract the images features
-	a PCA on the features 

The classification trained on the features is almost perfect.

The results were saved on a bucket AWS S3 in parquet format; a csv file containing PCA results was also saved.

## Acquired Skills

-	Use cloud tools to manipulate data in a Big Data environment
-	Identify cloud tools for setting up a Big Data environment
-	Parallelize operations with Pyspark


