# Disaster Response Pipeline Project

# Introduction
This Project is required as a part of the Data Science Nanodegree Program of Udacity. The initial dataset contains pre-labelled tweet and messages from real-life disaster situations. The aim of the project is to build a Natural Language Processing tool that categorize messages after natural disaster.

### The Project is divided in the following Sections:

- Processing Data, ETL Pipeline for extracting data from source, cleaning data and saving them in a proper database structure.
- Machine Learning Pipeline for training a model to be able to classify text message in categories.
- Web App for showing model results in real time.

# Files structure

- data: folder contains sample messages and categories datasets in csv format<br>
|- disaster_categories.csv # data to process<br>
|- disaster_messages.csv # data to process<br>
|- process_data.py # python code takes as input csv files(message data and message categories datasets), clean it, and then creates a SQL database <br>
|- disasterMessagesDatabase.db # database to save clean data to <br>
- app: contains the run.py to deploy the web app.<br>
| - template<br>
| |- master.html # main page of web app<br>
| |- go.html # classification result page of web app<br>
|- run.py # Flask file that runs app<br>
- models<br>
|- train_classifier.py # code to train the ML model with the SQL data base<br>
|- Classifier.pkl # saved model<br>
|- ETLPipelinePreparation.ipynb: process_data.py development process<br>
|- MLPipelinePreparation.ipynb: train_classifier.py development process <br>
- README.md<br>




# Installation
python (=>3.6) <br>
pandas
<br>numpy
<br>sqlalchemy
<br>sys
<br>plotly
<br>sklearn
<br>joblib
<br>flask
<br>nltk

## Instructions:
1- Run the following commands in the project's root directory to set up your database and model.

2- To run ETL pipeline that cleans data and stores in database ``` python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/disaster_messages.db```

3- To run ML pipeline that trains classifier and saves ``` python models/train_classifier.py data/disaster_messages.db models/model.pkl```

4- Run the following command in the project directory to run your web app. ```python app/run.py```

5- Go to http://0.0.0.0:3001/


## Note
- Pleas download the model from here: ### and add it to models folder
