# Stock-market-prediction
Its a hybrid model consisting of a CNN model to get the sentimet index. Then, a LSTM model to get the final predicted values.  
To get the sentiment data , I used the GDLET Project API to get the news headlines from moneyControl, Financial Express and economic times.  
Uisng word tokenizer and Wor2Vec , each of the headlines were converted into a vector of size 100. The choice of vector size as 100 is used as previously some research indicated that vector size of 100 to 300
gave better results.Each sentence of n words is considered as a 2D Matrix of dimension n x k. The lenght of n in our case is
20 and k is 100.The CNN model has 3 convolution layers, Max Pooling layer and 2 fully connected layer.
CNN Model


![Screenshot 2023-08-18 151406](https://github.com/tanmay154agrawal/Stock-market-prediction/assets/124059983/b8e42b90-7efc-4b0c-afa8-0baa7b1ca239)

Then,I firtly used different feature sets i.e. High,Low,Open,Close,Volume to predict the Close Price in the future.The sentiment Index model was first excluded , then incorporated into the historical price model to judge its impact.  
3 models were used which are RNN , CNN and LSTM. The results are shown below.  


![Screenshot 2023-09-12 231143](https://github.com/tanmay154agrawal/Stock-market-prediction/assets/124059983/fac2040d-4c10-468c-86e7-cd2093d30245)



![Screenshot 2023-09-12 231321](https://github.com/tanmay154agrawal/Stock-market-prediction/assets/124059983/8f31277b-5c4f-4ea9-a8bc-b03831be9baa)


![Screenshot 2023-09-12 231441](https://github.com/tanmay154agrawal/Stock-market-prediction/assets/124059983/ca39795e-9aba-4225-979d-c6bf85fa635c)


![Screenshot 2023-09-12 231535](https://github.com/tanmay154agrawal/Stock-market-prediction/assets/124059983/2da38e0c-0e9b-4a7a-b320-4ec486700885)


![Screenshot 2023-09-12 231626](https://github.com/tanmay154agrawal/Stock-market-prediction/assets/124059983/2e866d41-08ce-4f43-9adb-6e7fcf2acae3)


![Screenshot 2023-09-12 231706](https://github.com/tanmay154agrawal/Stock-market-prediction/assets/124059983/0ef7c3ec-b6bf-4bd6-822e-5f29ca78f5c2)

As it is clear that LSTM performs the best , so for further analysis LSTM is used.  

![Screenshot 2023-09-12 231925](https://github.com/tanmay154agrawal/Stock-market-prediction/assets/124059983/03a4e8a1-8d08-4709-9fab-ef147ce7b86f)  

![Screenshot 2023-09-12 232028](https://github.com/tanmay154agrawal/Stock-market-prediction/assets/124059983/248b3e5f-eb57-437b-bf38-f4e736d3fbb7)


So, the sentiments do affect the prices of stock market.  
File gdlet.ipynb is the script to get the sentiment data.  
DSS (Decision Support System) is the main file 
