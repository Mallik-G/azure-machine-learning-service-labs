# Model Training with AutoML

In this lab you will us the automated machine learning (Auto ML) capabilities within the Azure Machine Learning service to automatically train multiple models with varying algorithms and hyperparameters, select the best performing model and register that model.

## Exercise 1 - Get oriented to the lab files

1. In your virtual machine expand the folder `C:\LabFiles\azure-machine-learning-service-labs-master\starter-artifacts\visual-studio-code\04-automl`.<br/>
2. Expand the `data` folder. This folder contains the CSV file `UsedCars_Affordability.csv` which contains the complete data set with labels (Affordable is 1 for affordable, 0 for not affordable).<br/>
<img src="images/data1.jpg"/><br/>
3. To run a lab, start Visual Studio Code from taskbar and click on **Open folder**:<br/>
<img src="images/code.jpg"/><br/>
4. Select `04-automl` folder which is under `C:\LabFiles\azure-machine-learning-service-labs-master\starter-artifacts\visual-studio-code\`<br/>
<img src="images/auto.jpg"/><br/>
``
Please install if you are prompted to install Python. Ignore other extensions because we don't require for this lab.
``
5. Select the `04-automl.py` python file from **Explorer**<br/>
6. For Interpreter command go to **View** and Select **Command Palette** (⇧⌘P).<br/>
<img src="images/lab26.jpg"/><br/>
7. Click on **Python: Select Interpreter**. This may take 4-5 minutes<br/>
<img src="images/select.jpg"/><br/>
8. Once you setup the python interpreter, select conda environmen `azure_automl`<br/>
<img src="images/python.jpg"/><br/>
9. `04_automl.py` is the Python file you will step thru executing in this lab.<br/>
10. Refer below image for executing each cell i.e, just above all steps in below exercises<br/>
<img src="images/lab04.jpg"/><br/>

## Exercise 2 - Train a model using AutoML

This lab built upon the lessons learned in the previous lab but is self-contained so you work through this lab without having to run a previous lab.<br/><br/>
1. Begin with **Step 1**. In this step you are loading the data prepared in previous labs and acquiring (or creating) an instance of your Azure Machine Learning Workspace. Copy **subscription_id**, **resource_group** and **workspace_region** from your Environment Detail Page will be using these values in below step<br/>
<img src="images/env.jpg"/><br/>
2. Set the values for **subscription_id**, **resource_group** and **workspace_region** that you copied in above step. And give any unique name for **workspace_name**<br/>
<img src="images/aut.jpg"/><br/>
3. Execute **Step 1**. You will be prompted to log in to your Azure. Use the **Azure credentials** that are given in your **Environment Detail Page**. If you didn't get **Login** prompt go to **Internet Explorer**<br/>
<img src="images/sign.jpg"/><br/>
4. Copy the **Password** from **Environment Detail Page** and Paste in Sign in page<br/>
<img src="images/pass.jpg"/><br/>
5. Check the Output in **Python Interactive**<br/>
<img src="images/lab21.jpg"/><br/>
6. To train a model using **AutoML** you need only provide a configuration for AutoML that defines items such as the type of model (classification or regression), the performance metric to optimize, exit criteria in terms of max training time and iterations and desired performance, any algorithms that should not be used, and the path into which to output the results. This configuration is specified using the `AutomMLConfig` class, which is then used to drive the submission of an experiment via `experiment.submit`. When AutoML finishes the parent run, you can easily get the best performing run and model from the returned run object by using `run.get_output()`. **Execute** Step 2 to define the helper function that wraps the AutoML job submission.<br/>
<img src="images/lab22.jpg"/><br/>
7. In **Step 3**, you invoke the AutoML job. **Execute** Step 3.<br/>
<img src="images/lab23.jpg"/><br/>
8. Try out the best model by using Step 4.<br/>
<img src="images/lab24.jpg"/><br/>

## Exercise 3 - Register an AutoML created model

1. You can register models created by **AutoML** with Azure Machine Learning just as you would any other model. **Execute** Step 5 to register this model.<br/>
<img src="images/lab25.jpg"/><br/>
