## Lab Setup.
Lab setup includes the following tasks needs to be performed.
1. Create Google Cloud Account.
2. Create Amazon Web Services Account.
3. Generate keys.
4. Setup Google Cloud.
5. Install tools. (For Windows)

### 1. Create Google Cloud Account.

Create a new Gmail address and SignUp for google cloud in URL (https://cloud.google.com) 

Note:   In order to create an account you need a valid credit card/ debit card with working phone number.
        I would prefer to use a new gmail address instead of using your personal one.
        In account type while registering select `Individual` rather than using `Business` which is default.

Once you login and after few minutes you will look the console page as follows.

![image](https://user-images.githubusercontent.com/29029753/41230048-f4276c2a-6d9b-11e8-8cfa-bbd2a6d51bea.png)

From there you can navigate to `Compute Engine` to create servers.

![image](https://user-images.githubusercontent.com/29029753/41230112-38088438-6d9c-11e8-8a43-b8dd06c7f641.png)

We will come back and create the servers in upcoming section.

### 2. Create Amazon Web Services Account.

Our course includes AWS topics too are going to be covered. So you do require a AWS account also. Please try to SignUP for AWS also.
Refer the following link to create an account.

https://www.youtube.com/watch?v=ux1T3j6_MXc

### 3. Generate keys.

You can generate the keys (SSH Keys Private and Public) in two ways.
    
####    a. From Web tools
You can generate Public Keys and Private Keys in the following URL.
https://qsandbox.com/tools/private-public-keygen
Open the URL and click on generate.
 ![image](https://user-images.githubusercontent.com/29029753/41242316-cbac7d0a-6dbc-11e8-89a1-262093c37df5.png)
Then copy the content as save them with notepad.
Copy Private Key and Save As devops.pem in home directory.
    ![image](https://user-images.githubusercontent.com/29029753/41242599-a108fa28-6dbd-11e8-938d-e094f2fc161a.png)
    ![image](https://user-images.githubusercontent.com/29029753/41242694-d4b4b7c2-6dbd-11e8-8d52-08e4176de342.png)
Copy Public Key and Save As devops.pub in home directory.
    ![image](https://user-images.githubusercontent.com/29029753/41242755-fedeba70-6dbd-11e8-827a-c5ed69daa073.png)
    ![image](https://user-images.githubusercontent.com/29029753/41242811-20edba76-6dbe-11e8-9442-b500cb19f1cd.png)

####    b. From GitBash (Need installation of this tool)
You need to download this tool based on your architecuture.

32 bit: https://github.com/git-for-windows/git/releases/download/v2.17.1.windows.2/Git-2.17.1.2-32-bit.exe
64 bit: https://github.com/git-for-windows/git/releases/download/v2.17.1.windows.2/Git-2.17.1.2-64-bit.exe
Install with default options.
Then open GitBash icon from StartMenu.
![image](https://user-images.githubusercontent.com/29029753/41243174-2aa5c454-6dbf-11e8-8f8c-69afd4c39c33.png)
Run the following commands in the same sequence.
![image](https://user-images.githubusercontent.com/29029753/41243324-7e0ebfec-6dbf-11e8-8e21-b851505bde47.png)
```
$ rm -rf devops*
$ ssk-keygen -q -f devops -N ''
$ mv devops devops.pem
```
### 4. Setup Google Cloud.     
You need to configure google cloud in order to access with the key which are generated with step.

####    a. Setup Firewall.
Goto firewall rules under VPC network. 
![image](https://user-images.githubusercontent.com/29029753/41243706-7812362c-6dc0-11e8-85ef-77de139342af.png)
![image](https://user-images.githubusercontent.com/29029753/41243752-9c4943a0-6dc0-11e8-9b25-af4c1ea2a474.png)
Add/Change the following parameters to add new.
    <b><b>Name</b></b>: `all`
    <b><b>Targets</b></b>: `All instances in the network`
    <b><b>Source IP ranges</b></b>: `0.0.0.0/0`
    <b><b>Protocols and ports</b></b>: `Allow all`    
Then click on <b><u>Create></b></u>

