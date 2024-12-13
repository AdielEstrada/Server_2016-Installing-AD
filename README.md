# Part 2 - Installing Active Directory and Renaming Server Environment

> [!NOTE]
> You should be logged in as an administrator on your Server 2016 VM before starting this part of the project. You set it up in the previous page (Part 1).

## Renaming Server Environment
The first step is opening File Explorer (1). You right-click on "This PC" (2), and click "Properties" (3).

<img src="https://i.ibb.co/ZSPcf86/1.png">

> Note: Another way of accessing this panel is going to the search icon, and searching c:. Then you right-click "This PC" and so on. In fact, for this lab, this is what I did. However, opening File Explorer should give you the same results and involves less steps in my opinion.

After we click on properties, Control Panel will pop-up. Where it says "Computer Name, domain, and workgroup settings", click on the shield Icon that says "Change Settings". A pop-up called "System Properties" will appear. We want to click on the box that says "Change", as shown. 

 <img src="https://i.ibb.co/BjLhcrH/1-1.png">

 A "Computer Name/Domain Changes" screen will pop-up. Under "Computer Name", type "Server2016". Click ok, and accept the restart that it will ask of you.
 
<img src="https://i.ibb.co/2y0YfCg/4-change-computer-name.png">

This will set the name of our server. Having such a simple name will allow us to easily access this resource later on. In an actual environment, a more descriptive name might be used, but for now, this works just fine. 

> Note: You can make sure the changes were made after the restart by doing what we did in the beginning. You go to File Explorer, you right-click on This Pc and click on Properties. Under Computer Name, Domain, and Workgroup settings, you should see that now the Computer Name is Server2016.

## Adjusting Server for Best Performance
Under the Computer Name, Domain, and Workgroup settings, we will click on "Change Settings", the same shield icon we clicked to change the name of the server. But now, under System Properties, we will click on Advanced. We are looking for the Performance settings. 

<img src="https://i.ibb.co/0qvqTwR/8-performance-settings.png">

This will take us to a screen called "Performance Options". Here, under "Visual Effects", we will click "Adjust for Best Performance". This will help so that the virtual environment runs as smooth as possible. 

<img src="https://i.ibb.co/2NtG18y/9-adjust-for-best-performance.png">

Once that is done, we could close everything. 

## Installing Active Directory

Press the Windows key, and open "Server Manager". Then, under the "Manage" tab, click "Add Roles and Features". 

<img src="https://i.ibb.co/4Zdry53/12-manage-add-roles-and-features.png">

The Add Roles and Features Wizard pops up. This is just a fancy name for a tool that will help us install Active Directory. On this screen, it shows a list of pre-requisites that you need to verify before continuing. On an actual server environment, do verify this. But, for our environment, everything is fine. You can click next. 

<img src="https://i.ibb.co/LJMKYs9/13-next.png">

Then, it will prompt you to select an installation type. There is two options available: "Role-based or feature-based installation", and "Remote Desktop Services installation". Role-based installation allows you to set up the features you want to download on your server environment. For now, we don't have to worry about Remote Desktop Services, so we will just make sure that we have selected a Role-based installation. Then we click next. 

<img src="https://i.ibb.co/QdJt8Qn/14-select-installation-type.png">

From there, it will ask you to select a destination server. Make sure Server 2016 is selected (or whatever you named your project). Click next.

<img src="https://i.ibb.co/YpKn8q5/15-select-destination-server.png">

Then, we are asked to select the roles we want to add. Look for and click on "Active Directory Domain Services". You will notice that a pop-up will appear asking you to confirm whether you want a suite of features to be added that are required for Active Directory Domain Services. We need these services, so click on "Add Features". 

<img src="https://i.ibb.co/G01zjZS/16-Active-directory-domain-services.png">

Make sure Group Policy Management is selected. Then, we can click next. A screen that is titled "Active Directory Domain Services" will pop-up. It will list a few of the next steps you need to take to install Active Directory. We can click next. 

<img src="https://i.ibb.co/WH3Q0gZ/18-next.png">

A summary of the feaatures to be installed will be displayed on the screen. Once you're sure those are the features you want to install, click "Install". A progress bar will appear. Once the progress bar is filled up, an option will appear that says, "Promote this server to a domain controller". Click on that option.

<img src="https://i.ibb.co/7NX9nT1/21-promote-this-to-a-domain-controller.png">

A deployment configuration screen will pop up. There are 3 deployment options: "Add a domain controller to an existing domain", "Add a new domain to an existing forest", and "Add a new forest". To understand this, a forest is the highest level of organization possible in Active Directory. In our situation, we don't have a forest, so we will need to create one. Click on "Add a new forest". 

Then, it will ask you to specify the domain information. In the real world, we need to be careful with the name we choose, since it could confilct with other domain names. But, since this is just for a lab environment, the name we choose doesn't matter, as long as it ends with ".com", ".local", or something similar. For this instance, I chose the name "adielit.local". Where it says "Root Domain Name", you can write the name for the domain. Click next.

<img src="https://i.ibb.co/yXn0Fcr/22-add-a-new-forest.png"> 

The Domain Controller Options Window will appear. Here, we will only focus on creating a recovery password. Make sure you don't lose it! So, where it asks you to type the DSRM password, create a password. Usually, this would be a strong password. But, for ease of use in this project, you can choose a simple password. Type it in and click next. 
