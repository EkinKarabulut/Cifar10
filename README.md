# Run:ai x Weights & Biases Demo - Cifar10 Classification

Kubernetes is an open-source orchestration system that simplifies deployment, scaling, and management of containerized applications. However, its complexity can lead to productivity loss and neglect of data science tasks for teams. The Run:ai and Weights & Biases (WandB) integration addresses these challenges, providing data scientists with streamlined workflows, enhanced experiment tracking, and simplified infrastructure management.

## Key Benefits
The Run:ai and WandB integration provides data scientists with several key benefits, including:

* **Streamlined workflows**: The integration simplifies infrastructure usage on Kubernetes, allowing data scientists to focus on their core data science tasks. They can easily manage their experiments and allocate resources based on their specific needs.

* **Enhanced experiment tracking**: The integration enables data scientists to track their experiments in real-time and collaborate more easily with their team members. They can monitor their experiments and get insights into their performance, making it easier to improve their models.

* **Simplified infrastructure management**: The integration abstracts away the complexity of Kubernetes, making it easier for data scientists to run their experiments without requiring specialist knowledge in infrastructure management.

## Demo Overview
This demo showcases the seamless integration of Run:ai and WandB with Cifar10 classification in comparison to traditional Kubernetes setup. Cifar10 is a dataset of 60,000 32x32 color images in 10 classes, with 6,000 images per class. The objective is to classify the images into their respective classes using deep learning algorithms.

## Setup with Run:ai

To set up the demo with Run:ai and WandB, follow these steps:

### Prerequisites
  * An existing Kubernetes cluster
  * Run:ai installed on top of the Kubernetes cluster
  * A WandB account

### Step 1: Login to your Run:ai account on the UI

Go to the Run:ai login page and enter your credentials.

![Alt text](images/login_screen.png?raw=true "Title")

### Step 2: Create a new workspace

Click on the "Workspaces" tab and start creating a new workspace for the demo.

![Alt text](images/cifar10_demo_workspaces.png?raw=true "Title")

![Alt text](images/cifar10_new_workspace.png?raw=true "Title")



### Step 3: Choose the project and compute resource

Select the "cifar10-classification" project and choose the compute resource that best suits your needs. Be aware that these are ready made templates and if you have more different resources for your projects, you can always add a new type of resource with clicking "New Compute Resource" section.

![Alt text](images/cifar10_name_workspace.png?raw=true "Title")

![Alt text](images/cifar10_choose_compute.png?raw=true "Title")

### Step 4: Choose the data source and create the workspace

* We can also select a data source or create a new one. For this demo, we will download the cifar dataset on the fly within the Jupyter Notebook. Therefore, mounting a data source is not required. After choosing the datas source, you can create the workspace by clicking the "Create Workspace" button.

![Alt text](images/cifar10_choose_data_source.png?raw=true "Title")

### Step 5: Access the JupyterLab interface

Once the pod is deployed, click "Connect" to access the JupyterLab interface without any additional portforwarding configurations.

![Alt text](images/cifar10_jupyter_connection.png?raw=true "Title")

![Alt text](images/cifar10_jupyter_interface.png?raw=true "Title")

### Step 6: Clone your Github repository and download required libraries

Clone the Github repository where your project currently resides. Then, download all libraries in the requirements.txt file, or create a specific image of the required libraries (This can also be done by creating a specific images of the required libraries).

![Alt text](images/cifar10_clone_your_repo.png?raw=true "Title")

![Alt text](images/cifar10_download_requirements.png?raw=true "Title")

### Step 8: Start training with your first model

You can now go ahead and start training with your first model in the Jupyter Notebook.

![Alt text](images/cifar10_ready_to_go.png?raw=true "Title")

### Step 9: Initialize WandB

Initialize WandB for the run and configuration under the project name "cifar10-project". After running this cell, WandB will ask for our API key. You can find it under "User Settings > Danger Zone > API Key" in your Wandb account. We copy the key and click enter.

![Alt text](images/cifar10_initialize_wandb.png?raw=true "Title")

![Alt text](images/cifar10_api_key.png?raw=true "Title")

### May the force of GPUs be with you!

Now we can see that it created a wandb folder to log our runs and started synching the run (this one is called "happy-music"). We can simply click on the link and head to the WandB dashboard to see first insights.

![Alt text](images/cifar10_wandb_ready.png?raw=true "Title")

We can observe all of our runs within this project on the dashboard, filter them out depending on different configuration and compare the loss and accuracy graphs of the runs in real time. This gives us the opportunity to interfere quickly when the results does not look as expected without worrying about the resources and configurations. We can also create sweep jobs, where different runs with different parameters that we want to observe can be run in the queue, while giving us more visibility over the correlation between different variables and metrics. 

![Alt text](images/cifar10_wandb_dashboard.png?raw=true "Title")

![Alt text](images/cifar10_wandb_logs.png?raw=true "Title")

