<p align="center">
<img src="https://i.imgur.com/AeiqMDZ.png"/>
</p>

<h1>Network File Sharing and User Permissions</h1>
In this tutorial, we will experiment with Network Security Groups. 
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Domain Controller/Client Machine)
- Remote Desktop
- Shared Network Files

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

</p>
<p>
In this lab we will be setting up different shared network files & designate access permissions using the same Virtual Machines set up in our Active Directory lab. We will create folders on our Domain Controller Virtual Machine (DC-1) and share them on the "mydomain.com" network, and each folder will have certain individual permissions. Only designated users will be able to view specific files. We'll start by going to the C:/ drive on the DC-1 machine and create four folders: "read-access," "read/write-access," "no-access," and "accounting".
</p>
<br />

<p>
<img src="https://i.imgur.com/k70dozS.png"/>
</p>
<p>
After creating our four folders we will now set the permissions of three of the folders in DC-1. Set the folders to the appropriate permissions: "Read-access" should be read only for domain users, "read/write access" should have read/write permissions for domain users, and "no-access" should have read/write permissions for domain admins only. After the folders have been created, share them on the "mydomain.com" network so that the Client-1 machine can view them.
</p>
<br />

<p>
<img src="https://i.imgur.com/wcpB5Ex.png"/>
</p>
<img src="https://i.imgur.com/hku11Pt.png"/>
<p>
If we log in to the client machine with a normal user account we can test out the shared files we just created. As you can see, the permissions that we set are working properly.
</p>
<br />
<p>
<img src="https://i.imgur.com/CGQ8yaO.png"/>
</p>
<img src="https://i.imgur.com/f9TldBO.png"/>
<p>
</p>
Go back to our DC-1. In Active Directory Users and Computers create a security group called "Accountants" the users assigned to this security group will be the only ones allowed to view the Accountants folder. We have to share the accountants folder just like we did for our first three access folders. Normal users will not have access to this folder, only those with account group access. If we wanted to give a normal user access to the accounting folder they would have to be a part of the "Accountants" security group.
</p>
<br />
<p>
<img src="https://i.imgur.com/QADy92Z.png"/>
</p>
<img src="https://i.imgur.com/BUm3L2Q.png"/>
</p>
<img src="https://i.imgur.com/fH8fU7b.png"/>
