<h1>Learning Microsoft Intune, 365, and Entra Administration (IN PROGRESS)</h1>

<br />
<h2>Description</h2>
I had planned for this to be a project where I explore the characteristics of Microsoft Intune, however, because many Microsoft applications are interconnected I ended up obtaining experience with Microsoft 365, Intune, Entra, and Azure in some capacity. I first explored Microsoft 365 Admin Center where I managed creating and assigning roles and licenses to standard and guest accounts, deleting accounts, and created a security group to assign the users to which redirected me to Azure. I also configured a Microsoft 365 group for organizational wide private email, as well as discovered how to reset passwords of users and mailboxes from with 365 Admin Center. I then stumbled into Microsoft Intune Admin Center where I created multiple device configurations to secure web browsing with Google Chrome and overall endpoint best security practices. Within Intune, I also configured the deployment of the Microsoft 365 app suite to users. When I moved to Microsoft Entra Admin Center, I changed the default user role permissions to ensure only administrators can register applications and create security groups. Also within Entra I deployed enterprise Zoom to all users and changed acceptable authentication methods to include a passkey, Microsoft Authenticator, or temporary access pass for administrators.

<h2>Utilities Used</h2>

- <b>Microsoft 365 Admin Center</b> 
- <b>Microsoft Intune Admin Center</b>
- <b>Microsoft Entra Admin Center</b>
- <b>Microsoft Azure</b>


<h2>Lab Overview:</h2>

<p align="center">
After signing up for Microsoft Intune, setting up the domain KJHomeLab, and creating my first account, I was met with the Microsoft 365 Admin center which suprised me. I did not know that much about Intune or 365, and because I was brought to the 365 Admin Center I thought it would be a good time to explore that. <br/>
<img src="https://github.com/user-attachments/assets/c8df6a18-0b59-4d5b-a13b-e026896ab488" alt="Intune and 365"/>
<br />
<br />
The first thing under the Home tab which I was already in, was Users, so I thought it would be a good idea to create some users as I might use them later to test administrative methods. I created multiple users with basic priviliges and a helpdesk account as every administrator other than global. There is also the ability to delete users as well. If, for instance, you licensed the user with someting such as Intune, when the user is deleted you will gain the license back.<br/>
 <img src="https://github.com/user-attachments/assets/49e916ee-bd71-4376-b5c2-cab338f01220" alt="Intune and 365"/>
 <img src="https://github.com/user-attachments/assets/e16b2006-f20c-4a12-ac5e-aa0957fffa0d" alt="Intune and 365"/>
  <img src="https://github.com/user-attachments/assets/efa1bc09-6e0c-43c0-baab-2aced195b3f3" alt="Intune and 365"/>

<img src="https://github.com/user-attachments/assets/d59e7fff-c77f-43c2-9891-1f93a2dfa89a" alt="Intune and 365"/>
<br />
<br />
I then created a Security Group called Engineering Department and assigned some users to it. I also created a Microsoft 365 group which appears to be a shared email list. I added all the users, set it to private meaning that only those invited or added to the group could receive or send emails from it. It seems like a nice tool to have to send out bulk emails to a specific group or even the entire organization.<br/>
<img src="https://github.com/user-attachments/assets/94c49142-4394-4828-afae-e21a9cfe9314" alt="Intune and 365"/>
 <img src="https://github.com/user-attachments/assets/27591f10-06a5-4c07-bf56-ce94af01e891" alt="Intune and 365"/>
 <img src="https://github.com/user-attachments/assets/43315b2e-1ebc-4cc3-a8c7-0778b6588949" alt="Intune and 365"/>
<br />
<br />
From within 365 Admin Center you can reset user's password or password protected mailboxes similar to Active Directory Users and Computers. When resetting a password there is an option to automatically create a password or the admin can manually create a password if there is a password naming scheme in the organization.<br/>
<img src="https://github.com/user-attachments/assets/feb7db72-7426-4111-935a-4e9c7b709898" alt="Intune and 365"/>
<img src="https://github.com/user-attachments/assets/29137489-cc5c-441d-ab75-494877b0e105" alt="Intune and 365"/>
<br />
<br />
Interestingly, when I chose to create a guest user, it launched me into Microsoft Azure rather than staying within 365 Admin Center like creating standard user accounts. Moreover, there were considerably more fields to fill out when creating the guest user in Azure than 365.<br/>
<img src="https://github.com/user-attachments/assets/97a7fdf5-1282-45ec-9f21-6a6cfcabb489" alt="Intune and 365"/>
 <img src="https://github.com/user-attachments/assets/e17f324b-f2ce-4996-a03c-2071ea1508b0" alt="Intune and 365"/>
<br />
<br />
As I neared the bottom of 365 Admin Center, the Admin center group redirected me to different pages such as Microsoft Defender when clicking on security and Microsoft Intune Admin Center when I clicked on Endpoint Manager.  <br/>
<img src="https://github.com/user-attachments/assets/26b375d4-5172-4311-8d43-ef91b9835d7e" alt="Intune and 365"/>
<br />
<br />
Microsoft Intune Admin Center had completely different settings and configurations than 365 Admin Center, and seemed to focus on devices and configurations similar to Group Policy Objects in Active Directory. I first created a Configuration called Internet Browsing. I configured some basic rules to increase the security and limit some ability of users when using Google Chrome which could be set as the organization's only allowed web browser. The rules I set were: disabling third party screen capture, restrict HTTP connections, and block external extensions from being installed. When applying the device configurations, Intune allows you to include or exclude groups for the policy which is great for different departments that have different needs and permissions.<br/>
<img src="https://github.com/user-attachments/assets/2219dc91-d356-40bc-8705-5a887aa02111" alt="Intune and 365"/>
<img src="https://github.com/user-attachments/assets/1262bbce-17f7-462a-ba39-57cdfc5344bd" alt="Intune and 365"/>
<img src="https://github.com/user-attachments/assets/24d409e5-039c-4395-81a9-2644c36b35d4" alt="Intune and 365"/>
<img src="https://github.com/user-attachments/assets/69ae6889-772c-455b-bd76-a4e31bd55150" alt="Intune and 365"/>
<img src="https://github.com/user-attachments/assets/16c119dd-27d2-4202-bef5-35fbd786e8e3" alt="Intune and 365"/>
<br />
<br />
For more practice I created another Device Configuration this time to enforce basic security handening for the organization. The rules included: Deny all access to removable storage devices, disable users from logging in with temporary profiles, and enabling session logging. For this rule, I was added all devices and all users to the included groups to ensure everyone and everything is covered by this policy.<br/>
<img src="https://github.com/user-attachments/assets/2b924dba-5f5f-4082-8baf-230aacbf608c" alt="Intune and 365"/>
<br />
<br />
Another very useful ability that Intune Admin Center provides is remote application installation. In this example, I deployed all Microsoft 365 apps for Windows 10 and later endpoints. Furthermore, configuration options were very specific such as, if I only wanted specific apps within the suite, whether to download the 32 or 64-bit architecture and what version to install. This seems very similar to the tool Deploy by PDQ I experimented with in a past project.<br/>
<img src="https://github.com/user-attachments/assets/fc553d89-77a4-4462-9aee-ed9b9b955904" alt="Intune and 365"/>
<br />
<br />
Within Intune Admin Center when I clicked on the Users field on the left I was once again redirected to different Microsoft product, this time Entra Admin Center. When in Entra, I saw the Users I had createad in 365 Admin Cetner earlier, and under user settings I changed some of the default settings to ensure users can not make changes to Entra or 365.<br/>
<img src="https://github.com/user-attachments/assets/704c4622-11ee-489a-9282-2449c27d3769" alt="Intune and 365"/>
<br />
<br />
There was another tool within Entra Admin Center that like Intune Admin Center allowed me to remotely install enterprise applications. I chose to deploy Zoom to the users in the domain. The process of adding users or groups to receive the application was similar, it lists the users, but at the top you can choose add group to more efficently add specific users already defined. <br/>
<img src="https://github.com/user-attachments/assets/628691e3-628a-40e8-968e-b267dffd6926" alt="Intune and 365"/>
<img src="https://github.com/user-attachments/assets/dd1d355c-6675-4466-a3f0-b7925231919f" alt="Intune and 365"/>
<br />
<br />



<h2>Thoughts</h2>
This project was very interesting as it kept taking turns and redirecting to applications I had no initial intention of using. However, I was gladly suprised. I initially only wanted to learn about Intune, but was able to learn about several other Microsoft tools and systems. In a perfect world, there is no reason for all them no be tied together in one administration tool, however, at least within say 365 Admin center, clicking on endpoints opens Intunes to configure endpoints. All of the products were fairly straightforward. Potentially in a future project I will add the Intune licenses to users on a virtual machine and do active configuration rather than theoretical. That would make for even more learning opportunities. 
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
