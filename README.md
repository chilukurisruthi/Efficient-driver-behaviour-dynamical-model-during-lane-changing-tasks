# Efficient-driver-behaviour-dynamical-model-during-lane-changing-tasks
This work introduces an efficient driver behaviour dynamical model designed to simulate lane-changing tasks in a realistic and computationally feasible manner.demonstrating potential applications in autonomous vehicle testing, advanced driver-assistance systems (ADAS), and traffic simulation platforms.
In propose work author utilizing cybernetic single-loop transfer function models employing McRuer’s theory to select precise model with minimum number of parameters. Model selection will be calculated using Machine Learning cross validation function with mean square error (MSE). Model with minimum parameters and minimum MSE error will be selected as best model. 
Author utilizing cybernetics McRuer’s theory with minimize object function called ‘tfest’ to select minimal number of parameters. McRuer’s theory is based on cybernetics function which works on feedback systems and control theory. According to this theory, the human operator acts as a biological feedback controller having a transfer function, FR(s), and adapting his or her behaviour to the dynamics of the controlled element, FC(s). Knowing the dynamic model, FC(s), enables us to define the structure of the appropriate model of the controller.
Author has evaluate model with 4 different parameters as Pole1 to Pole4 and all this model were experimented on 10 different driver behaviour and then predicted driver control action and all models with minimal parameters predicting close behaviour. Finally each model performance with minimum parameters is evaluated with the help cross validation MSE error.
All experimentations are shown in the form of graph and then model efficiency calculated with minimal parameters and model original parameters. To train and test each model performance author has developed his own dataset with in-house build simulator but not publish on internet so we did experiment with available dataset on the internet.
Dataset can be download from below URL
https://www.kaggle.com/datasets/shashwatwork/driving-behavior-dataset
Abstract: We test an approach to modelling the car driver behaviour during simulated lane changing tasks, aiming to obtain a sufficiently precise model in the simplest possible form, namely, with a small number of parameters. Various applications of such models are available in the literature. Based on a recent review of the research to date, the cybernetic single-loop transfer function models employing McRuer’s theory are applied. The purpose of the presented method is to evaluate the optimal structure of the transfer function via cross-validation as a technique known from machine learning. The experiments utilize a driving simulator with in-house developed software; this configuration facilitates acquiring the data at the desired sampling frequency and in a manner that ensures the repeatability of the test process scenarios. Using the cross-validation results, we evaluate the second-order model with a derivative state and a reaction delay component as an optimal structure for approximating the measured data, which originated from a set of measurements on 92 active drivers. Even though more complex driving tasks could require high-order models, drivers control action during our specific experiment is described through only four parameters. The parameters are jointly determined by the current driver’s mental state and the testing conditions defined in our scenario. Since the parameters are related to his/her dynamical behaviour, they allow easier mutual comparison of the drivers than complex models with many parameters. The results are verified via establishing a relationship to the multi-loop model presented in the recent literature. The larger dataset enables evaluating the confidence intervals of the drivers’ parameters which is inconvenient with 4 to 10 drivers commonly presented in the relevant sources.
Modules Information
To implement this project we have designed following modules
1)	Registration Here: new user can sign up with the application
2)	User Login: user can login to system
3)	Load & Process Driver Dataset: using this module user can upload and process driver behaviour dataset and then split dataset into train and test where McRuer’s theory will use this train data to train model with different number of parameters and then choose minimal parameters as optimize parameters.
4)	Run Dynamic Behaviour Model: driver dynamic behaviour model will be evaluated using ML model and McRuer’s theory and then visualize MSE graph and driver action control graph
5)	Parameter Identification: this module will run algorithm to find best minimal parameters compared to ML default parameters.
SCREEN SHOTS
Install python 3.7.2 and then install all packages given in requirements.txt file and then install MYSQL and create database by copying content from ‘database.txt’ file and paste in MYSQL console
To run project double click on ‘run.bat’ file to start python server and then will get below page
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/3d73fe8e-dd37-48e4-994f-50fc4dc4d333" />

 
In above screen application start running McRuer’s theory minimize function to calculate minimum number of parameters and then started python web server. Now open browser and enter URL as http://127.0.0.1:8000/index.html and then press enter key to get below page
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/037a46b8-474a-4c5a-b892-64b5cf49334f" />

 
In above screen click on ‘Registration Here’ link to get below page
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/6c5f51d4-fb0c-4de9-9df9-b406b9e4815e" />

 
In above screen user is entering sign up details and then press button to get below page

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/d9cc3996-88df-4e7a-9fe9-435bb5dc2868" />

 
In above screen user sign up process completed and now click on ‘User Login Here’ link to get below page

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/3016e539-4f03-4b8c-b3cb-f8033ad0bf68" />

 
In above screen user is login and after login will get below page
 <img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/b2ea8d90-9326-4e13-b643-c565f798251c" />

In above screen user can click on ‘Load & Process Driver Dataset’ link to get below page
 <img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/69babace-57f4-4d0b-99fd-63eeeed8f602" />

In above screen selecting and uploading driver lane dataset and then click on buttons to get below page
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/6c766eae-b301-45e5-9c16-db3e4cb5d93e" />

 
In above screen in blue text can see number of records available in dataset and then can see different lane actions in dataset and can see number of chosen drivers. In black text can see dataset values and now click on ‘Run Dynamic Behaviour Model’ link to predict driver behaviour and then will get below output
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/6119ade8-1cf6-4fa7-baa2-4f5ba7b9f945" />

 
In above screen in first graph can see MSE calculation by each model for 10 different drivers and in above graph can see all models predicting different behaviour with minor error as bars in graphs for different driver having minimum changes. In second graph displaying driver control prediction from 4 different models where x-axis represents Time and y-axis represents Driver control prediction and each different colour line represents different model driver action and can see all models predicted driver action equally as all lines are overlapping with minor gap. Now click on ‘Parameter Identification’ link to get below page

<img width="940" height="489" alt="image" src="https://github.com/user-attachments/assets/d1ac4185-cc95-44be-b00c-8d26038f1fa5" />

 
In above screen we are displaying chosen minimal parameters for each model and by default each model having 100 estimators and then McRuer’s transfer function chosen minimal parameters and then showing difference as the model efficiency. In above output first column contains Model Name, second columns contains total parameter estimator and 3rd column contains selected minimal parameter and 4th column contains model efficiency values.
 
 
