# Medicine Demand Prediction and Health Expense Prediction & Planning

## Medicine Demand Healthbox
This model specifically deals with prediction of demand based on a particular dataset. It works on the basis of timeseries where appropriate features are extracted to get the best type of model then a xgboost training model.
<br>
Link to the website: https://healthbox.azurewebsites.net/
<br>
Link to the base repository: https://github.com/tiprock-network/MedicineDemand-TimeSeries/tree/healthbox
<br>
The notebook that build up the data story of the model: https://github.com/tiprock-network/MedicineDemand-TimeSeries/blob/healthbox/demand-timeseries.ipynb

<br>

![](https://github.com/tiprock-network/MedicineDemand-TimeSeries/blob/main/assets/homehealthbx.png?raw=true)

### Below is a clear illustration of the process of using the website for prediction.

Access the website, choose your type of commodity demand and then finally get a prediction.
![Prediction](https://github.com/tiprock-network/MedicineDemand-TimeSeries/blob/main/assets/prediction.png?raw=true) | ![Input](https://github.com/tiprock-network/MedicineDemand-TimeSeries/blob/main/assets/entry.png?raw=true)

### Healthbox Tools Used

* VS Code
* Azure Web Apps

### Recommendation
This project is especially essential for pharmaceutical companies and local hospitals in that it helps them make medicine more accessible by determining future demand hence saving time in procument of medicine.

## Health Expense Prediction & Planning
This app allows the user to predict their Health Expense using a Machine Learning Model and then get a detailed personalized plan to save funds for it.

This section comprised of 5 parts:
1. Data Exploration using Python of the [dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)
2. Azure AutoML Regression Model to predict the health expenses for an individual based on various input parameters.
3. Using Open AI to create a customized Health Expense Saving Plan for the individual.
4. A Power Automate Flow to consume the Azure AutoML Model's endpoint and connect it to the Power App
5. Power Apps based interface to bring it all together

|Starting Screen|Output 1 |Output 2 |
:-------------------------:|:-------------------------:|:-------------------------:
![starting page](assets/startScreen.jpg) | ![output 1](assets/output1.jpg) | ![output 2](assets/output2.jpg)

### Features
This app allows the user to:
* Predict Health expenses based on various parameters like age, sex, bmi, number of children and whether they are a smoker or not
* Uses a custom built Azure Auto ML model integrated to Power Apps using Power Automate Flow
* Provides a customized plan to save for health expenses based on inputs and the result of the model using Open AI's API

### Power Automate Flow
Uses a Power Automate Flow to pass the input to the model and get the results back.

* The flow uses HTTP to POST the inputs to the Model Endpoint
* It then uses Parse JSON to parse the output
* Finally sends it back to the Power App

A screenshot for the flow:
![starting page](assets/PowerAutomateFlow.jpg)

### Azure Auto ML Model

#### Data Exploration:
![Charges](assets/charges.png) | ![Pie Chart](assets/piechart.png) | ![Dataset](assets/dataset.jpg)

#### Model:
![End Point](assets/endpoint.jpg) | ![Model Details](assets/modeldetails.jpg) | ![Residuals](assets/residuals.jpg) | ![Results](assets/results.jpg)

Deployed Model Endpoint URL: [Link](http://c692c678-bd90-41d8-ac5f-5d1d140d196e.centralindia.azurecontainer.io/score)

Deployed App URL: [Link](https://apps.powerapps.com/play/e/cf46801e-aa6d-4a32-a161-692e900c34cc/a/6f7695e5-11d7-4fa1-96e9-bd0aae6bd6f7?tenantId=84c31ca0-ac3b-4eae-ad11-519d80233e6f)
