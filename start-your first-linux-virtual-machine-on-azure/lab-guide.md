# Module 0: Introduction to Azure Portal

   * [Exercise 01: Sign Up for Pre-configured Environment](#exercise-01-sign-up-for-pre-configured-environment)
 
 ### Lab Overview
This lab will take you through Azure login and portal experience and the pre-requisite environment.

### Option 1: Using Preconfigured Environment

### Time Estimate

10 minutes

### Exercise 1: Sign Up for pre configured environment

In this exercise, you will create a source environment.
1.	**Navigate** to bitly link which was provided by instructor and register by providing all required information and **clicking** on **SUBMIT button**.<br/>
<img src="images/signin.png"/><br/>

2. Once registration is accepted, you will be automatically redirected to the lab activation page. Now, it is advised to save a copy of the URL on the browser, which has the activation id. **Click** on the **Launch Lab** button.<br/>
<img src="images/launch.png"/><br/>

3. You will see the environment details soon below.<br/>
<img src="images/credentials.png"/><br/>
Please ensure to take the values assigned to your deployment.

### Exercise 2: Log into your Azure Portal and Verify access to the Subscription

In this exercise, you will log into the **Azure Portal** using your Azure credentials and you will verify the type of role you are assigned in this Subscription.
1.  **Navigate** to https://portal.azure.com and login (from the previous step).
2.  **Enter** the **Username** which was displayed in the previous window and **click** on **Next**.<br/>
<img src="images/azuresigninpage.png"/><br/>
3.	In the Stay signed in? pop-up window, click **No**. **Enter** the **Password** and click on **Sign in**.<br/>
<img src="images/passwordsignin.png"/><br/>

### Exercise 3: Create a Linux virtual machine in the Azure portal

Azure virtual machines (VMs) can be created through the Azure portal. The Azure portal is a browser-based user interface to create Azure resources. This quickstart shows you how to use the Azure portal to deploy a Linux virtual machine (VM) running Ubuntu 18.04 LTS. To see your VM in action, you also SSH to the VM.
**Create SSH key pair**
You need an SSH key pair to complete this quickstart. If you already have an SSH key pair, you can skip this step.

1.Open a bash shell and use ssh-keygen to create an SSH key pair. If you don't have a bash shell on your local computer, you can use the Azure Cloud Shell.
2.In the menu at the top of the page, select the >_ icon to open Cloud Shell.
3.Make sure the CloudShell says Bash in the upper left. If it says PowerShell, use the drop-down to select Bash and select Confirm to change to the Bash shell.
4.Type ssh-keygen -t rsa -b 2048 to create the ssh key.
5.You will be prompted to enter a file in which to save the key pair. Just press Enter to save in the default location, listed in brackets.
6.You will be asked to enter a passphrase. You can type a passphrase for your SSH key or press Enter to continue without a passphrase.
7.The ssh-keygen command generates public and private keys with the default name of id_rsa in the ~/.ssh directory. The command returns the full path to the public key. Use the path to the public key to display its contents with cat by typing cat ~/.ssh/id_rsa.pub.
8.Copy the output of this command and save it somewhere to use later in this article. This is your public key and you will need it when configuring your administrator account to log in to your VM.

Create virtual machine

1.Choose Create a resource in the upper left corner of the Azure portal.
2.In Popular, select Ubuntu Server 18.04 LTS.
3.In the Basics tab, under Project details, make sure the correct subscription is selected and then choose to Create new under Resource group. Type myResourceGroup for the name of the resource group and then choose OK.
4.Under Instance details, type myVM for the Virtual machine name and choose East US for your Region. Leave the other defaults.
5.Under Administrator account, select SSH public key, type your user name, then paste in your public key. Remove any leading or trailing white space in your public key.
6.Under Inbound port rules > Public inbound ports, choose Allow selected ports and then select SSH (22) and HTTP (80) from the drop-down.
7.Leave the remaining defaults and then select the Review + create button at the bottom of the page.

8.On the Create a virtual machine page, you can see the details about the VM you are about to create. When you are ready, select Create.

Connect to virtual machine
Run this command in Azure CLI
ssh azureuser@10.111.12.123
