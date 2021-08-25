При создании эксперимента AutoAI, вы можете подключить сэмпл данных. Это позволит увидеть весь процесс AutoAI.

В этом разделе описывается, как сохранить конвейер (пайплайн) как модель Watson Machine Learning, опубликовать модель и использовать ее для скоринга и последующего просмотра результатов прогнозирования.

## Предварительное условие
Создайте проект в Watson Studio со связанным экземпляром службы Machine Learning Service.

## Обзор действий
Из этого руководство  Вы узнаете - как взять модель, построенную в AutoAI, развернуть и оценить полученную модель, а также увидеть, как формируется прогноз. 
Выполните следующие действия в Watson Studio:

* Build and train the model
* Deploy the trained model
* Test the deployed model

### Step 1: Build and train the model
* 1.1 Specify basic model details
From the Assets page of your project in Watson Studio, click Add to project and choose AUTOAI EXPERIMENT.
In the page that opens, fill in the basic fields:
  - Specify a name and optional description for your new model.
  - Choose From Sample and click the Bank marketing sample data.
  - Building from sample data
  - Confirm that the IBM Watson Machine Learning service instance that you associated with your project is selected in the Machine Learning Service section.
  - Click Create.
* 1.2 Add training data

![training](https://github.com/vperrinfr/network_intrusion/blob/master/images/autoai_bank_sample_data.png)

* 1.3 Train the model
In the guided experience, the column labeled “CLASS” is automatically selected for the model. The default metric for a binary classification is ROC/AUC.
  - Choosing a prediction column
  - Click Run experiment. As the model trains, you will see an infographic that shows the process of building the pipelines.
  - Building model pipelines
For a list of algorithms, or estimators, available with each machine learning technique in AutoAI, see: [AutoAI implementation detail](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/autoai-details.html?audience=wdp)

![autoai_bank_sample_pipeline_build](https://github.com/vperrinfr/network_intrusion/blob/master/images/autoai_bank_sample_pipeline_build2.png)

* 1.4 Choose a pipeline
Once the pipeline creation is complete, you can view and compare the ranked pipelines in a leaderboard.

![leaderboard](https://github.com/vperrinfr/network_intrusion/blob/master/images/autoai_bank_sample_leaderboard2.png)

Choose Save model from the action menu for the pipeline with a rank of 1. This saves the pipeline as a Machine Learning asset in your project.

### Step 2: Deploy the trained model
Before you can use your trained model to make predictions on new data, you must deploy the model.

You can deploy the model from the model details page. You can access the model details page in one of these ways:

Click on the model name in the notification displayed when you save the model.
Open the Assets page for the project containing the model and click the model name in the Machine Learning Model section.
From the model details page:

  - Click the Deployments tab.
  - Click Add Deployment.
  - In the page that opens, fill in the fields:
      - Specify a name for the deployment.
      - Select “Web service” as the Deployment type.
      - Click Save.
  - After you save the deployment, click on the deployment name to view the deployment details page.

### Step 3: Test the deployed model
You can test the deployed model from the deployment details page in **three** ways:

### Test with a form
On the Test tab of the deployment details page, click the icon to Provide input data using form, enter test data, and click Predict to see the result.

![autoai-test-with-form.png](https://github.com/vperrinfr/network_intrusion/blob/master/images/autoai-test-with-form.png)

### Test with JSON code
On the Test tab of the deployment details page, click the icon to Provide input data as JSON and enter the following test data:

```{"input_data":[{"fields": ["duration", "protocol_type", "service", "flag", "src_bytes", "dst_bytes", "land", "wrong_fragment", "urgent", "hot", "num_failed_logins", "logged_in", "num_compromised", "root_shell", "su_attempted", "num_root", "num_file_creations", "num_shells", "num_access_files", "num_outbound_cmds", "is_host_login", "is_guest_login", "count", "srv_count", "serror_rate", "srv_serror_rate", "rerror_rate", "srv_rerror_rate", "same_srv_rate", "diff_srv_rate", "srv_diff_host_rate", "dst_host_count", "dst_host_srv_count", "dst_host_same_srv_rate", "dst_host_diff_srv_rate", "dst_host_same_src_port_rate", "dst_host_srv_diff_host_rate", "dst_host_serror_rate", "dst_host_srv_serror_rate", "dst_host_rerror_rate", "dst_host_srv_rerror_rate"], "values": [**ARRAY_OF_VALUES**]}]}```

### Test with a Notebook

You can easily call the deployed model through a Jupyter Notebook.

![notebook.png](https://github.com/vperrinfr/network_intrusion/blob/master/images/notebook.png)
