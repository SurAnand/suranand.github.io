---
layout: post
title: Notes on Azure Fundamentals
comments: true
---

# Notes on Azure Fundamentals

## Today 14 Sep 2020

This long-scrolling post is nothing but the notes I took while learning AZ Fundamentals. Most of it is my own writing, with a few details directly copied from the Azure Documentation. Images are almost always taken from the Azure website, with a few being my screenshots.

Since the whole content is already freely available on Microsoft website, I believe there is no copyright issue in this. If there is, please alert me.

> Because, ***Ignorantia juris non excusat!***, or [something like that](https://en.wikipedia.org/wiki/Ignorantia_juris_non_excusat) ;-)

> Ref: https://aka.ms/azfunpath

### Matt Hester <img src="../public\matt_hester.jpg/" width=200> Garette Bundy <img src="../public\garette_bundy.jpg/" width=200>

<img src="../public\1.jpg">

|*******Passing score = 700 and more*******|

> **Those who plan to take the [AZ 900](https://docs.microsoft.com/en-us/learn/certifications/exams/az-900) exam should at any cost read the [Exam Skills Outline](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE3VwUY) document. The importance of this cannot be stressed more.**

---

# Notes from the [Azure Fundamentals](https://docs.microsoft.com/en-us/learn/paths/azure-fundamentals/) | Part-1

## Tour of Azure Services

#### Azure Services into Broad Categories

1. Compute Services
  - VMs, Containers, Serverless Computing including Microservices  
2. Cloud Storage
  - Disks attached to VMs, structural formats like fileshares and databases
3. Networking
  - Configure and control your networking to send traffic in and out of Azure, like private networks
4. App Hosting
  - Run web apps, marketplace which gives ready solutions
5. Artificial Intelligence
  - ML & prebuilt cognitive services, big data analytics
6. Internet of Things
  - Integrate things with networks
7. Integration
  - Logic apps, orchestration, etc.
8. Security
  - Integrated into every aspect of Azure Services; control who has access to what, etc.

Check this Image below to see Azure Services on a high level.

<img src="https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/media/3-azure-services.png#lightbox">

#### Most Commonly Used Service Categories

- Compute
- Networking
- Storage
- Mobile
- Databases
- Web
- IoT
- Big data
- AI
- DevOps

> What are virtual machine scale sets?
> Refer this [link](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/overview#:~:text=Azure%20virtual%20machine%20scale%20sets%20let%20you%20create%20and,group%20of%20load%20balanced%20VMs.&text=Scale%20sets%20provide%20high%20availability,a%20large%20number%20of%20VMs.)

> Azure virtual machine scale sets let you create and manage a group of load balanced VMs. The number of VM instances can automatically increase or decrease in response to demand or a defined schedule. Scale sets provide high availability to your applications, and allow you to centrally manage, configure, and update a large number of VMs. With virtual machine scale sets, you can build large-scale services for areas such as compute, big data, and container workloads.

#### Azure Compute Services

* VMs are also called as **Compute Nodes**
* <u>*Azure VMs*</u> - provides Windows and Linux VMs
* <u>*Azure VM Scale Sets*</u> - create and manage a group of load balanced VMs, set to automatically increase or decrease the no. of VMs in response to demand or schedule
* <u>*Azure Kubernetes Service*</u> - manage containerized VMs
* <u>*Azure Service Fabric*</u> - manage microservice based application setups; runs anywhere on other clouds, on Linux or on-prem
* <u>*Azure Batch*</u> - run parallel and HPC batch jobs scheduled on multiple compute nodes
* <u>*Azure Container Instances*</u> - run containerized applications without provisioning servers or VMs
* <u>*Azure Functions*</u> - This needs a special mention. So I wrote about it below.

<hr>

#### Serverless Computing - The coming-together of Azure Functions, Logic Apps and Event Grid
<p>&nbsp;</p>
<img src="https://sec.ch9.ms/ch9/c4ed/16f3632b-8cef-4e0e-ac4b-d08e5c2ec4ed/Serverless_960.jpg?v=c422b9a7e2f5fdac62d92c69dd98da0a0d9c72fd6b0e06be8cd1b4ec147b052f">
<p>&nbsp;</p>
**This part needs a special mention because this is just one feature out of the many coming out the concept of <u>Serverless Computing or Serverless Application</u>**.

- Serverless computing is essentially a framework within which the client just worries about writing code so their application work seamlessly, without having to spend their time on the number of VMs they need, the amount of storage they need, the kind of networking they need, the level of security they need, etc. All these things will be automatically scaled up and down based on the app's requirement and other parameters.
- I just watched a simple 20 minutes [YouTube video](https://www.youtube.com/watch?v=RddQOxDcdFg) on this subject and the use case shown here is really "**stupid simple**".
- Serverless Computing on Azure works with 3 most critical services provided by the platform.
  - Azure Functions
  - Azure Logic Apps
  - Azure Event Grid
- The video above is essential to understand how these 3 features work in harmony to ensure a serverless app runs seamlessly, just taking care of some manual work which otherwise would have taken number of hours, or even days and number of employees workload.
- But to put it simply, here is the use case shown in the above video.
  - It is called **Employee Onboarding process**. Now we all know how boring and repetitive this is and how much time the HR staff end up spending on. Azure Functions, Logic Apps and Event Grid functionalities will take care of this whole process, and produce results in perhaps 1-2% time and with 1-2% of the efforts.
- I may sound exaggerating, but I am honestly impressed when I saw the demo in the video.
- The only issue is that the staff who create and maintain such workflows should be really efficient, and would need a positive encouraging support from the bosses.

#### Azure Networking Services

> **<u>NETWORKING</u> - Linking compute resources and providing access to applications is the key function of Azure networking.** (*Copied from the Azure Fundamentals documentation web page*)

The work *Networking* is surely one of the most enigmatic things in Computer Science and Technology. No matter how much is said and written about it, it is still one of the most fascinating areas.

Particularly when networking is being talked about in Data Center and Cloud related subjects, it's attractiveness gets amp'ed up quite hardly, because it surely needs a good grasp of quite a few subjects, including mathematics, geography, weather science, electronics, engineering, and what not. Of course, that's why people work in teams with members of their own specialities.

So, not much of notes can be written on this subject, because it usually takes months to years to learn this subject anyway.

> As summary, Azure can do pretty anything and everything you can think of under the title "Networking", mostly automatically.

<img src="../public\Azure Networking.jpg">

---

#### Azure Storage

Azure provides 4 types of Storage Services.
1. <u>Blob Storage</u> - for very large data, such as videos
2. <u>File Storage</u> - usual file server
3. <u>Queue Storage</u> - for queuing and delivering messages between applications
4. <u>Table Storage</u> - for unstructured data, usually a NoSQL store, independent of schema

All storage services come with the following features:
- High availability and Redundancy
- Automatic Encryption and RBAC
- Scalability
- Maintenance by Microsoft
- Most of these storage services can also be configured to be accessible from mobile phones, made for all flavors - iOS, Windows and Android, along with Push notifications.

#### And More ....

Azure Services include a lot of other services that, similar to networking, cannot be explained in a single post like this.

For instance, Azure Database Services offer a wide range of services that include use cases with almost all flavors of database types, such as MySQL, NoSQL, PostgreSQL, CosmosDB, MariaDB, etc.

Azure Web Services include *all things web applications* - notification hubs, API management, real time web functionalities, etc.

Azure IoT, Big data, AI and DevOps include a vast number of services that enable and enhance daily activities in the modern technology-driven world, right from letting a vacuum cleaner determine whether its job for the day is complete or not depending on the dust it can sense on the floor, up to visual analytics of a poacher in Amazon forest who attempted to poach a rhino and got caught, first in the sensor-based camera in the forest and then by the police before they could run more than 10 km in the forest.

### Take Away, truly! Microsoft Learn Sandbox

Sandbox is nothing but Azure resources made available for the learn to practice and get some hands-on feel on the Azure Services. This is free of cost and time-bound resource. It is really helpful to get the hang of how managing your cloud on Azure portal feels like.

Also, you would be able to clearly understand the workflow. Once it is clear in our mind what we want to create, depending on that object, we can see what the workflow is. For example, before you do anything, you will have create a **Resource Group**. Anything and everything you create begins with this step. And then the individual workflows will begin. You will go to marketplace and choose a ready-made service, or will create something from the scratch, either by creating a new VM, or a new DB, etc.

Another very crucial critical skill one learn using the Sandbox is to practice the [*Azure CLI*](https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/6-exercise-cloud-shell). This is surely an added feather in the hat, once learned sufficiently. You almost never have to log into the Azure portal and everything can be managed just from the comfort of your terminal window. Thanks to Microsoft's open collaboration with Linux, you can manage your Azure services both from Windows and Linux OS command line tools.

---

# Notes from the [Azure Fundamentals](https://docs.microsoft.com/en-us/learn/paths/azure-fundamentals/) | Part-2

## Tour of Azure Services

### Azure **Regions** and Data Centers

Azure has established its data centers in a large number of geographical regions, spanning almost all the continents. It has a lot of data centers in its motherland USA, with a few dedicated, network-isolated, ***specialized*** data centers for US government departments. Outside, they have setups in the EU, Australia, New Zealand, UAE, Qatar, Saudi Arabia, Israel, India, Chine and the far east.

This vast set of regional setups ensure that the clients who depend on Azure Services can always choose the closest possible region to ensure faster reach, and multiple data centers in most regions ensure the business continuity.

Some regions in the far east, for example China, are not maintained by Microsoft, but by a Chinese company called [21Vianet](https://www.21vianet.com/).

<img src="https://docs.microsoft.com/en-us/learn/modules/explore-azure-infrastructure/media/2-regions-large.svg#lightbox">
<p>&nbsp;</p>

But in Azure technical terms, ***Regions*** are different from ***Geographies and Availability Zones***.

Azure divides *Geographies* into *Regions* for various purposes, such as US West, Australia Central, South India, etc.
- One of the ways they divided the geographies is based on the compliance requirement, therefore the regions in these geographies and the data centers in those regions can be setup based on the same compliance and regulatory requirements.
- Another reason is customer-centric. Clients who wish to address the **data residency or sovereignty** requirements can also benefit from this *geographies* concept.
- One more critical purpose is to ensure a whole region failure does not impact those business who focus on business continuity and high availability more than anything else, and thereby become fault-tolerant. For example, international banks.

##### Geographies are divided into Americas, Europe, Asia Pacific, Middle East and Africa

Finally, **Availability Zones**. These are separate data centers within a particular region. Sometimes, one zone can have multiple data centers.

> Availability Zones are primarily for VMs, managed disks, load balancers, and SQL databases. Azure services that support Availability Zones fall into two categories:
- <u>Zonal services</u> – you pin the resource to a specific zone (for example, virtual machines, managed disks, IP addresses)
- <u>Zone-redundant services</u> – platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).

#### So,
   - One or more data centers in an Availability Zone ...
   - One or more Availability Zones in a Region ...
   - One or more Regions or Region Pairs in a Geography !!!

In addition, there are also ***Region Pairs***. A region pair consists of two regions physically at least 300 miles away from each other, with the second one working as a fail-over the moment the first one is down due to any major cause, such as a natural disaster.
