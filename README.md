![](RackMultipart20231109-1-ksigmi_html_5e51c278365924fe.png)

# Microsoft Azure Mini Project

**By**

**Mr. Praful Bhalerao**

**Mr. Chandru Shankar**

**Mr. Yash Chari**

**Project Name = Azure Pipelines Kubernetes Deployment**

**Step 1: Create service connection between azure portal and azure dev ops.**

To create the connection, you need to first have an azure subscription, then go to azure dev ops website and go to project setting and go to service connection.

Service connection can be made between azure portal and azure dev ops by inputting all the necessary ports id numbers and linking all the necessary protocols for the connection.

Click on create service connection.

![](RackMultipart20231109-1-ksigmi_html_df76dba84770d007.png)

Then Select the Azure Resource Manager option and Next.

![](RackMultipart20231109-1-ksigmi_html_c6c06b0cd66573e0.png)

Then select the Service principal (manual) option and select next.

![](RackMultipart20231109-1-ksigmi_html_254897984439cec3.png)

Then select the subscription option and then provide the Subscription id from azure portal, Subscriptions, and provide it the type of subscription you have.

![](RackMultipart20231109-1-ksigmi_html_5381afa4211ef47a.png)

Then Go to azure portal's Microsoft intra and then go to default directory and there you can find your service principal key and Tenant id.

![](RackMultipart20231109-1-ksigmi_html_8937fa8e0deed32e.png)

And then click on verify.

Give the service connection name and then Grant all the access permissions and you will be set with a service connection.

![](RackMultipart20231109-1-ksigmi_html_2dad9b2fe9af6355.png)

**Step 2: Create azure container registry and azure Kubernetes cluster**

Azure Container Registry provides a secure and scalable way to store and manage container images, while Azure Kubernetes Service enables easy deployment and orchestration of containerized applications, making them a powerful combination for container-based workloads in the Azure ecosystem.

Go to azure portal and Search Container Registry.

![](RackMultipart20231109-1-ksigmi_html_9544c69dcb5f4f12.png)

Create container Registry

![](RackMultipart20231109-1-ksigmi_html_a58172d1b17d1998.png)

Fill all the basic details such as Resource Group, Name of the registry, region and provide it with Pricing plan and then Create.

![](RackMultipart20231109-1-ksigmi_html_d1c3fa8c7c5104b2.png)

![](RackMultipart20231109-1-ksigmi_html_698fc6f970f6a868.png)

Go to Azure portal and search Kubernetes services.

Create Kubernetes Cluster

![](RackMultipart20231109-1-ksigmi_html_5f5df24b52bbcab6.png)

Fill in basic details such as resource group, name, region, and provide pricing tier according to requirements.

![](RackMultipart20231109-1-ksigmi_html_dc1f5fc40ab68abb.png)

![](RackMultipart20231109-1-ksigmi_html_b672b7745ab6c06a.png)

![](RackMultipart20231109-1-ksigmi_html_c03f4c5a2f9f504d.png)

![](RackMultipart20231109-1-ksigmi_html_947dd7be59eda6af.png)

Then go to integration, and add the container registry you just created.

![](RackMultipart20231109-1-ksigmi_html_15d89a9bbdc11692.png)

![](RackMultipart20231109-1-ksigmi_html_c1e13562fc631b39.png)

![](RackMultipart20231109-1-ksigmi_html_69808a33056c9d23.png)

![](RackMultipart20231109-1-ksigmi_html_6fa91c2328d4f53b.png)

![](RackMultipart20231109-1-ksigmi_html_c3d367e1048e1435.png)

**Step 3: Import your project from your GitHub repository to Azure Devops**

Go to your GitHub account and open the repository in which you have saved your project

![](RackMultipart20231109-1-ksigmi_html_35223448d997e7b5.png)

Select the repository and copy the URL of the GitHub Repository in which you have your project.

![](RackMultipart20231109-1-ksigmi_html_731b5418a827535e.png)

Then Go to azure Devops and go to Repos and click on import repository.

![](RackMultipart20231109-1-ksigmi_html_7df288aac2596b59.png)

Paste the repository URL that you copied in the section, and import.

![](RackMultipart20231109-1-ksigmi_html_7ac903196d3a08a6.png)

![](RackMultipart20231109-1-ksigmi_html_185d4ed8f9beb3d7.png)

![](RackMultipart20231109-1-ksigmi_html_bb676dbb6829d301.png)

**Step 4: Create CI /CD pipeline, azure pipeline will actually push the image to the azure container registry, and then our azure pipeline will deploy the pods on the AKS cluster using that image**

A CI/CD pipeline connecting Azure Portal and Azure DevOps streamlines development, testing, and deployment, ensuring efficient and automated software delivery in a seamless Azure environment.

Go to Azure Devops, then go to pipeline and create new pipeline.

![](RackMultipart20231109-1-ksigmi_html_15ecb8910aa5a689.png)

Select azure repos git.

![](RackMultipart20231109-1-ksigmi_html_925673f2ab6fda29.png)

![](RackMultipart20231109-1-ksigmi_html_ef8a3390981880d8.png)

![](RackMultipart20231109-1-ksigmi_html_c1d5b371e1a9632e.png)

Delete the code and create another azure cli code by clicking on the show assistant option.

![](RackMultipart20231109-1-ksigmi_html_e4dadf9676795930.png)

![](RackMultipart20231109-1-ksigmi_html_8b73c3666d23ffd5.png)

![](RackMultipart20231109-1-ksigmi_html_6461910d7f403190.png)

Select the service connection name script type script location and script path.

![](RackMultipart20231109-1-ksigmi_html_4331f7e0239b5c78.png)

Provide the inline script and add.

![](RackMultipart20231109-1-ksigmi_html_b6913827a6f7295.png)

![](RackMultipart20231109-1-ksigmi_html_89812d538b4eb9ad.png)

Add this script line add the end and then save.

![](RackMultipart20231109-1-ksigmi_html_e76881bbbfcce5e.png)

![](RackMultipart20231109-1-ksigmi_html_58dc2ce35fd0fc89.png)

Then go to Run pipeline

![](RackMultipart20231109-1-ksigmi_html_773c5eed46b0c465.png)

Edit the pipeline and add the Azure Kubernetes Cluster to your azure pipeline.

![](RackMultipart20231109-1-ksigmi_html_4b76370b2c6c286.png)

![](RackMultipart20231109-1-ksigmi_html_dcef27e610d7ae3a.png)

Provide it with the basic details as given in the further documents.

![](RackMultipart20231109-1-ksigmi_html_e20f2896f49b75ac.png)

![](RackMultipart20231109-1-ksigmi_html_8d7f89793183cfdd.png)

![](RackMultipart20231109-1-ksigmi_html_d5ec4d366cd9cff8.png)

![](RackMultipart20231109-1-ksigmi_html_dabf8850bd8877e5.png)

![](RackMultipart20231109-1-ksigmi_html_96965514ab34ec80.png)

![](RackMultipart20231109-1-ksigmi_html_4e30aaee85edac29.png)

![](RackMultipart20231109-1-ksigmi_html_e87b71e9d3effc8b.png)

And save the code.

![](RackMultipart20231109-1-ksigmi_html_a580e040c0530983.png)

![](RackMultipart20231109-1-ksigmi_html_c0589a4746ceb187.png)

![](RackMultipart20231109-1-ksigmi_html_70254c00f1d19bb0.png)

Click on run pipeline.

![](RackMultipart20231109-1-ksigmi_html_42dc84634bd15885.png)

![](RackMultipart20231109-1-ksigmi_html_8287096948411db9.png)

Go to job

![](RackMultipart20231109-1-ksigmi_html_76fe7890a18be731.png)

Here you can see the Kubernetes code and the azure cli code, then go to azure cli and at the bottom you will find the ip address of your code.

![](RackMultipart20231109-1-ksigmi_html_e5d7b2918e21ce27.png)

![](RackMultipart20231109-1-ksigmi_html_cdf7b17a0137c8a4.png)

![](RackMultipart20231109-1-ksigmi_html_ee9f2fa48e4d5130.png)

![](RackMultipart20231109-1-ksigmi_html_3ebc64a174ac3a31.png)

Go to any browser of your choice and paste the ip address.

![](RackMultipart20231109-1-ksigmi_html_e601371b2e7d701a.png)

![](RackMultipart20231109-1-ksigmi_html_989ea28fbb29732a.png)

![](RackMultipart20231109-1-ksigmi_html_ee540f8c32f175d5.png)

![](RackMultipart20231109-1-ksigmi_html_31b6bffb5d006488.png)
