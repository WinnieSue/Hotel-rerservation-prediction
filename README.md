# Hotel Reservation Prediction

**Author**: Namutebi Winnie Susan

**Business problem**:

With over 100 clients calling in and others booking online, it is not easy to know which client who made a booking will honor their booking and actually check in as scheduled. Hotels find themselves between a rock and a hard place and they are struggling to know which client to take seriously. So a tool that can help do this is something that the hotel needs to know where to focus their time and resources.

**Data**

Source of data : Kaggle (https://www.kaggle.com/datasets/ahsan81/hotel-reservations-classification-dataset) 
The data includes information about clients who make a booking at the hotel. Each client is giving a booking ID, the number of adults, the number of children with them, the number of weeknights and weekend nights, the type of meal plan that they want, whether they need parking space or not, the type of room they want to reserve, the lead time, the arrival date, the market segment they are in, the proce of the room. The Hotel also records whwther this client is a repeat client and if they have honored or canceled their booking before. After all that, They recvord whether the client booked or not.

**Method**

The data had no missing values but we had both categorical and numerical values. Therefore I used the standard scaler and OneHotEncoder to prepare the data for preprocessing. The Year, Month and Date I changed the datatype to object so that I can OHE it instead of scale it because the values of year, month and date do not have magnitude. 

I made some visualizations to get a better understanding of the data and the relationships between different features.

The first visualization shows the relationship between a client being a repeated guest and the possibility of canceling or not canceling their booking

![p1](https://user-images.githubusercontent.com/122565105/230725579-866371c7-cfee-4b47-ae46-b6df5477c570.png)

In the visualization below, we see that the price of the room is highly affected by the number of people. but aslo we see that when the number exceeds 4, the price goes down. This shows that usually group bookings opt for the cheaper rooms.

![p2](https://user-images.githubusercontent.com/122565105/230725704-9f79b218-1e28-490e-a712-fd84d2d7ad81.png)

**MODEL**

I tried three different models; i.e., The logistic Regression model, the Random Forest Classifier and the Extreme Gradient Bossting model. I decided to deploy the Random Forest Classifier because it has the best F1 score as compared to the other two. I am using the F1 score as the metric for choosing the model becasue for our problem, both precision and recall are important and the F1 score puts them both into consideration. t

F1 score on the Booking status: 'Not Canceled' is 0.93

F1 score on the Booking stated: 'Canceled' is 0.85.

**RECOMMENDATIONS** 

I recommend this model to be used when bookings are made. It can help to minimize costs in the sense that a client who calls in or books online and cancels their booking may get the hotel not to hold a room for them and prepare meals for them yet their booking will not be honored. So with this model, we can use the various details about a client and know whether they will book or not.



