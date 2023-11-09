<a name="br1"></a> 

Microsoft Azure Mini Project

[**Project**](https://github.com/Chandrus28/azure-devops-pipeline-with-acr-and-aks)[** ](https://github.com/Chandrus28/azure-devops-pipeline-with-acr-and-aks)[Overview**](https://github.com/Chandrus28/azure-devops-pipeline-with-acr-and-aks)

· Project Name: Azure Pipelines Kubernetes Deployments .

· Group Members: Praful Bhalerao. Yash Chari. Chandru Shankar

· Date: 09/11/2023

**Prerequisites :**

· An Azure account with an active subscription. [Create](https://azure.microsoft.com/en-us/free/?WT.mc_id=A261C142F)[ ](https://azure.microsoft.com/en-us/free/?WT.mc_id=A261C142F)[an](https://azure.microsoft.com/en-us/free/?WT.mc_id=A261C142F)[ ](https://azure.microsoft.com/en-us/free/?WT.mc_id=A261C142F)[account](https://azure.microsoft.com/en-us/free/?WT.mc_id=A261C142F)[ ](https://azure.microsoft.com/en-us/free/?WT.mc_id=A261C142F)[for](https://azure.microsoft.com/en-us/free/?WT.mc_id=A261C142F)[ ](https://azure.microsoft.com/en-us/free/?WT.mc_id=A261C142F)[free.](https://azure.microsoft.com/en-us/free/?WT.mc_id=A261C142F)

· An Azure DevOps organization. [Create](https://learn.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops)[ ](https://learn.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops)[an](https://learn.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops)[ ](https://learn.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops)[account](https://learn.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops)[ ](https://learn.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops)[for](https://learn.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops)[ ](https://learn.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops)[free.](https://learn.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops)

**Services Used :**

· Azure Resource Group

· Azure Container Registry

· Azure Kubernetes Cluster



<a name="br2"></a> 

Youtube Video ---- <https://www.youtube.com/watch?v=i1-PczamCy4>

Video ---- [https://drive.google.com/file/d/1-](https://drive.google.com/file/d/1-L0ER6C32YxWJew2WpgpXaBQeF4p86md/view?usp=sharing)

[L0ER6C32YxWJew2WpgpXaBQeF4p86md/view?usp=sharing](https://drive.google.com/file/d/1-L0ER6C32YxWJew2WpgpXaBQeF4p86md/view?usp=sharing)

Project pdf url ----

[https://drive.google.com/drive/u/0/folders/1ajkyL7rIRLirshak8hk7M8a9](https://drive.google.com/drive/u/0/folders/1ajkyL7rIRLirshak8hk7M8a9QpaLjIlN)

[QpaLjIlN](https://drive.google.com/drive/u/0/folders/1ajkyL7rIRLirshak8hk7M8a9QpaLjIlN)

**Step 1: Create service connection between azure portal and azure**

**dev ops.**

To create the connection, you need to first have an azure subscription, then go to

azure dev ops website and go to project setting and go to service connection.

Service connection can be made between azure portal and azure dev ops by

inputting all the necessary ports id numbers and linking all the necessary

protocols for the connection.

Click on create service connection.



<a name="br3"></a> 

Then Select the Azure Resource Manager option and Next.

Then select the Service principal (manual) option and select next.



<a name="br4"></a> 

Then select the subscription option and then provide the Subscription id from

azure portal, Subscriptions, and provide it the type of subscription you have.



<a name="br5"></a> 

Then Go to azure portal’s Microsoft intra and then go to default directory and

there you can find your service principal key and Tenant id.

And then click on verify.

Give the service connection name and then Grant all the access permissions and

you will be set with a service connection.



<a name="br6"></a> 

**Step 2: Create azure container registry and azure Kubernetes cluster**

Azure Container Registry provides a secure and scalable way to store and manage

container images, while Azure Kubernetes Service enables easy deployment and

orchestration of containerized applications, making them a powerful combination

for container-based workloads in the Azure ecosystem.

Go to azure portal and Search Container Registry.

Create container Registry



<a name="br7"></a> 

Fill all the basic details such as Resource Group, Name of the registry, region and

provide it with Pricing plan and then Create.



<a name="br8"></a> 

Go to Azure portal and search Kubernetes services.

Create Kubernetes Cluster



<a name="br9"></a> 

Fill in basic details such as resource group, name, region, and provide pricing tier

according to requirements.



<a name="br10"></a> 

Then go to integration, and add the container registry you just created.



<a name="br11"></a> 



<a name="br12"></a> 



<a name="br13"></a> 

**Step 3: Import your project from your GitHub repository to Azure**

**Devops**

Go to your GitHub account and open the repository in which you have saved your

project



<a name="br14"></a> 

Select the repository and copy the URL of the GitHub Repository in which you

have your project.

Then Go to azure Devops and go to Repos and click on import repository.



<a name="br15"></a> 

Paste the repository URL that you copied in the section, and import.



<a name="br16"></a> 

**Step 4: Create CI /CD pipeline, azure pipeline will actually push the**

**image to the azure container registry, and then our azure pipeline**

**will deploy the pods on the AKS cluster using that image**



<a name="br17"></a> 

A CI/CD pipeline connecting Azure Portal and Azure DevOps streamlines

development, testing, and deployment, ensuring efficient and automated software

delivery in a seamless Azure environment.

Go to Azure Devops, then go to pipeline and create new pipeline.

Select azure repos git.



<a name="br18"></a> 



<a name="br19"></a> 

Delete the code and create another azure cli code by clicking on the show

assistant option.



<a name="br20"></a> 

Select the service connection name script type script location and script path.



<a name="br21"></a> 

Provide the inline script and add.



<a name="br22"></a> 

Add this script line add the end and then save.



<a name="br23"></a> 

Then go to Run pipeline

Edit the pipeline and add the Azure Kubernetes Cluster to your azure pipeline.



<a name="br24"></a> 

Provide it with the basic details as given in the further documents.



<a name="br25"></a> 



<a name="br26"></a> 



<a name="br27"></a> 



<a name="br28"></a> 

And save the code.



<a name="br29"></a> 



<a name="br30"></a> 

Click on run pipeline.



<a name="br31"></a> 

Go to job



<a name="br32"></a> 

Here you can see the Kubernetes code and the azure cli code, then go to azure cli

and at the bottom you will find the ip address of your code.



<a name="br33"></a> 



<a name="br34"></a> 

Go to any browser of your choice and paste the ip address.



<a name="br35"></a> 



<a name="br36"></a> 


