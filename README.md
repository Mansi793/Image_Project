# Fruit-Ripeness-Detection
This project aims to classify 6 types of fruit (apple, banana, orange, pomegranate, mango and papaya) into 3 classes of raw, ripe or rotten

## Data Collection
The model was trained on the dataset that was scraped from Google Images using selenium.


Our model will train on the following set of 18 total classes 

![Screenshot (107)](https://user-images.githubusercontent.com/62397380/161302893-86afb3eb-1f35-4c9f-85cb-77820d3144b5.png)


Each class has around 110 images to it(following is an example of what the ripe apple class folder contains)

![Screenshot (108)](https://user-images.githubusercontent.com/62397380/161303088-9a0512a0-2545-4db8-9a5f-f4ed02678cd1.png)

## Model Building and Training
I used transfer learning to import the MobileNetv2 model containing weights trained on imagenet dataset. To this base layer of MobileNetV2, we add our global spatial average pooling layer, a fully connected layer and a logistic layer at the end. I used ReLu activation function in all the layers except the last one which is the logistic layer, for which i used a the sigmoid activation function.

The model was trained for 5 epochs in two stages and this was the graph obtained:

![Picture1](https://user-images.githubusercontent.com/62397380/161310069-05783a93-5985-4781-9723-c8351dab3f4c.jpg)

Our model returned the following result:

![Fruit Ripeness](https://user-images.githubusercontent.com/62397380/161310731-2eb88126-5403-4647-8f1d-aebe52b2f220.jpg)



