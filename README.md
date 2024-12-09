# Part 2 - Installing Active Directory and Renaming Server Environment

> [!NOTE]
> You should be logged in as an administrator on your Server 2016 VM before starting this part of the project. You set it up in the previous page.

## Renaming Server Environment
The first step is openning File Explorer (1). You right-click on "This PC" (2), and click "Properties" (3).

<img src="https://i.ibb.co/ZSPcf86/1.png">

> Note: Another way of accessing this panel is going to the search icon, and searching c:. Then you right-click "This PC" and so on. In fact, for this lab, this is what I did. However, openning File Explorer should give you the same results and involves less steps in my opinion.

 After we click on properties, Control Panel will pop-up. Where it says "Computer Name, domain, and workgroup settings", click on the shield Icon that says "Change Settings". A pop-up called "System Properties" will appear. We want to click on the box that says "Change", as shown. 

 <img src="https://i.ibb.co/BjLhcrH/1-1.png">

 A "Computer Name/Domain Changes" Screen will pop-up. Under "Computer Name", type "Server2016". Click ok, and accept the restart that it will ask of you.
 
<img src="https://i.ibb.co/2y0YfCg/4-change-computer-name.png">

This will set the name of our server. Having such a simple name will allow us to easily access this resource later on. In an actual environment, a more descriptive name might be used, but for now, this works just fine. 

> Note: You can make sure the changes were made after the restart by doing what we did in the beginning. You go to File Explorer, you right-click on This Pc and click on Properties. Under Computer Name, Domain, and Workgroup settings, you should see that now the Computer Name is Server2016.

## Adjusting Server for Best Performance
Under the Computer Name, Domain, and Workgroup settings, we will click on "Change Settings", the same shield icon we clicked to change the name of the server. But now, under System Properties, we will click on Advanced.
