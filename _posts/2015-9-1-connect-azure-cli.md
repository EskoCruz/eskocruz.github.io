---
layout: post
title: Connect to Azure from Command-Line Interface (Azure CLI)
---

Connect to an Azure subscription from the Azure Command-Line Interface (Azure CLI)

If you don't have an account, you can create a free trial account in just a couple of minutes.  
For details, see [Azure Free Trial](https://azure.microsoft.com/en-us/pricing/free-trial/).

If you do not currently have a work or school account, and are using a personal account to log in to your Azure subscription, you can easily create one using the following steps.

Login to the Azure Portal, and select Active Directory.  

1. If no directory exists, select Create your directory and provide the requested information.  
2. Select your directory and add a new user. This new user is a work or school account.  
3. During the creation of the user, you will be supplied with both an e-mail address for the user and a temporary password. Save this information as it is needed later.  
4. From the Azure portal, select Settings and then select Administrators. Select Add, and add the new user as a co-administrator. This allows the work or school account to manage your Azure subscription.  
5. Finally, log out of the Azure portal and then log back in using the new work or school account. If this is the first time logging in with this account, you will be prompted to change the password.  
6. Make sure you see your subscriptions when you log in as the work or school account.  
  For more information on work or school accounts, see [Sign up for Microsoft Azure as an Organization](http://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).  
  

```
$ npm install azure-cli -g
```
or 
```
$ brew cask install azure-cli
```

---

```
$ azure account download
$ azure login -u myemail@azureonlineurl.com
```
or
```
$ azure login -u <username>
info:    Executing command login
warn:    Please note that currently you can login only via Microsoft organizational account or service principal. For instructions on how to set them up, please read http://aka.ms/Dhf67j.
$ Password: ************
|info:    Added subscription Free Trial                                        
info:    Setting subscription "Free Trial" as default
+
info:    login command OK
$ 
```




#### Resources:
- https://azure.microsoft.com/en-us/documentation/articles/xplat-cli-install/
- https://azure.microsoft.com/en-us/documentation/articles/xplat-cli-connect/
