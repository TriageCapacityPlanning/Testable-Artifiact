# How it works:
Our application predicts how many clinic slots a hospital will need to meet patient demand using a machine learning and simulation model. Slots are divided between triage classes which determine how urgently a patient needs to be seen. A certain amount (proprtion) of patients of each class need to be seen within a specific time frame. You can customize triage classes (the name, time-frame and proportion) in the Admin section.

Once you've configured the triage classes you go into the Interval prediction section to request a prediction. Predictions are done over intervals and with a specific confidence level. You can also specify how many runs of the simulation you would like to perform. Once you request a prediction you will recieve results broken down by triage class.

See below for a breakdown of pages and their applications

# Interval Prediction Page:
![alt text](https://github.com/TriageCapacityPlanning/Testable-Artifiact/blob/main/docs/triagepredictionUI.png "image 1")
1. The interval (start date - end date) that you want to get a prediction for  
2. Add an additional interval. For example if you wanted the breakdown of arrivals for a month week-by-week you could have an interval each week  
3. Reset all the intervals. This will remove all intervals except the first one  
4. Confidence level - how confident the model needs to be that it's prediction will all you to see your target proportion within a target time. The default is 95%  
5. Select how many simulations the model should run to come up with an estimate (default is 100 and we recommend staying around this because it will take a really long time to run more)  
6. Request the prediction - you will see your results in cards below  

# Admin: Clinic 1
![alt text](https://github.com/TriageCapacityPlanning/Testable-Artifiact/blob/main/docs/triageuploadUI.png "image 2")  
1. Name: the name of the triage class, change this to update the names of classes when you get a prediction  
2. Duration: How soon a patient within a given triage class needs to be seen.   
3. proportion: what percentage of patients within the given triage class need to be seen within the set duration  
4. save your changes  
5. select a csv file with historical data the model can be trained with. You can use (this one) for example  
6. upload the historical data. Currently there is no visual feedback but you can check to the console to see data was uploaded correctly  
