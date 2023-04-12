# Run:ai & WandB Demo - Cifar10 Classification

Kubernetes is an open-source orchestration system that simplifies deployment, scaling, and management of containerized applications. However, its complexity can lead to productivity loss and neglect of data science tasks for teams. The Run:ai and WandB integration addresses these challenges, providing data scientists with streamlined workflows, enhanced experiment tracking, and simplified infrastructure management.

## Key Benefits
The Run:ai and WandB integration provides data scientists with several key benefits, including:

* **Streamlined workflows**: The integration simplifies infrastructure usage on Kubernetes, allowing data scientists to focus on their core data science tasks. They can easily manage their experiments and allocate resources based on their specific needs.

* **Enhanced experiment tracking**: The integration enables data scientists to track their experiments in real-time and collaborate more easily with their team members. They can monitor their experiments and get insights into their performance, making it easier to improve their models.

* **Simplified infrastructure management**: The integration abstracts away the complexity of Kubernetes, making it easier for data scientists to run their experiments without requiring specialist knowledge in infrastructure management.

## Demo Overview
This demo showcases the seamless integration of Run:ai and WandB with Cifar10 classification in comparison to traditional Kubernetes setup. Cifar10 is a dataset of 60,000 32x32 color images in 10 classes, with 6,000 images per class. The objective is to classify the images into their respective classes using deep learning algorithms.

## Setup without Run:ai

Assuming an existing Kubernetes cluster, the following steps would be necessary without the Run:ai and WandB integration:

1. Create a Dockerfile that includes WandB installation, training script (with path), and other installations such as VSCode, Jupyter, Pytorch, etc.
2. Build the Docker image and push it to a private Docker repository.
3. Configure the deployment YAML file for Kubernetes, including
 * Container configurations, 
 * Resource specifics for the container (GPU, CPU, memory), 
 * WandB API key as an environment variable.
 * Networking details of the tools, such as an exposed port for Jupyter Lab to run.
4. Run the deployment with the container that was created.

For more information and details, please check out [this documentation](https://wandb.ai/site/articles/model-explorations-and-hyperparameter-search-with-w-b-and-kubernetes)

## Setup with Run:ai

Here we assume that there is an existing Kubernetes cluster and Run:ai is installed on top of it. 

* We first login to our account on the UI

![Alt text](login.png?raw=true "Title")

* Then we head to workspaces and create a new workspace 

![Alt text](workspaces.png?raw=true "Title")

![Alt text](new_workspace.png?raw=true "Title")

