[Home](https://jasonmorris1.github.io/cse15l-lab-reports/)

# CSE 15L: Setting up Visual Studio Code

[LAB 1 instruction Link](https://docs.google.com/document/d/1AO6RDoJnaWxMui-UFjEa_2bbQ4qcANpbIpPuV-awsOg/edit#)


## 1. Download VScode for your operating system [VSCODE link](https://code.visualstudio.com/download) :arrow_left:
<p align="center">
    <img src="assets/images/vscodeDownload.png" width = "500" alt="centered image" />
</p>

## 2. Install VSCODE :floppy_disk:

<h3 align="center">Accept the License Agreement</h3>

<p align="center">
    <img src="assets/images/vscodestep1.png" width = "500" alt="centered image" />
</p>

<h3 align="center">Select your preferences</h3>

<p align="center">
    <img src="assets/images/vscodestep2.png" width = "500" alt="centered image" />
</p>

<h3 align="center">Final Install step</h3>

<p align="center">
    <img src="assets/images/vscodestep3.png" width = "500" alt="centered image" />
</p>

<h3 align="center">Open Vscode</h3>

<p align="center">
    <img src="assets/images/vscodeOpen.png" width = "500" alt="centered image" />
</p>


## 3. Install OpenSHH (Windows Guide) :satellite:
[Microsoft Guide](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)

### Open Power shell and enter command to check if Openssh is already installed
``` bat
Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'
```
<p align="center">
    <img src="assets/images/powershell1.png" width = "500" alt="centered image" />
</p>

#### If Open SSH is not installed, install it with the following powershell command:

``` bat
# Install the OpenSSH Client
Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

# Install the OpenSSH Server
Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0
```


## 4. Connecting to Remote Server :computer:
1. **In VScode open a terminal in VSCode (Ctrl + `, or use the Terminal → New Terminal menu option).**

2. **Connect to the ieng6 server using ssh**
**Note: Replace cs15lsp22zz with your account name.**

```
$ ssh cs15lsp22zz@ieng6.ucsd.edu
```
**When prompted enter you password. Your results should look similar to this**

```
⤇ ssh cs15lsp22zz@ieng6.ucsd.edu
The authenticity of host 'ieng6-202.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no/[fingerprint])? 
Password: 
Last login: Sun Jan  2 14:03:05 2022 from 107-217-10-235.lightspeed.sndgca.sbcglobal.net
quota: No filesystem specified.
Hello cs15lsp22zz, you are currently logged into ieng6-203.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages  
ieng6-201   23:25:01   0  0.08,  0.17,  0.11
ieng6-202   23:25:01   1  0.09,  0.15,  0.11
ieng6-203   23:25:01   1  0.08,  0.15,  0.11

Sun Jan 02, 2022 11:28pm - Prepping cs15lsp22
```

## 5. Run some commands on the server :calling:
```
cd ~
cd
ls -lat
ls -a
ls <directory> where <directory> is /home/linux/ieng6/cs15lsp22/cs15lsp22abc, where the abc is one of the other group members’ username
cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/
cat /home/linux/ieng6/cs15lsp22/public/hello.txt
```

### Screen shot of some commands being run. 
<p align="center">
    <img src="assets/images/commands.png" width = "600" alt="centered image" />
</p>




## 6. Moving Files over SSH with scp :clipboard:


### Create a file name WhereAmI.java in VSCode with the following code:

``` java
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```
#### Run the code using javac and java in the terminal

```
PS C:\Users\jason\Documents\cse15l-lab-reports> javac .\WhereAmI.java
PS C:\Users\jason\Documents\cse15l-lab-reports> java WhereAmI
Windows 10
jason
C:\Users\jason
C:\Users\jason\Documents\cse15l-lab-reports
PS C:\Users\jason\Documents\cse15l-lab-reports> 
```

#### To copy the file to the server use the scp command
```
scp WhereAmI.java cs15lsp22ajb@ieng6.ucsd.edu:~/
```
* Note. You should be prompted to enter you password
#### Your result should look similar to this
```
PS C:\Users\jason\Documents\cse15l-lab-reports> scp WhereAmI.java cs15lsp22ajb@ieng6.ucsd.edu:~/
WhereAmI.java                                                     100%  311     1.0KB/s   00:00  
```

#### SSH back into the server and run the `ls` command

#### You should see the file in your home directory

```
[cs15lsp22ajb@ieng6-201]:~:54$ ls
CSE12_PA1  WhereAmI.class  WhereAmI.java  perl5  test
```
#### Run javac and java on the server

```
PS C:\Users\jason\Documents\cse15l-lab-reports> ssh cs15lsp22ajb@ieng6.ucsd.edu
Last login: Mon Nov 29 17:33:04 2021 from 100.83.55.225
quota: No filesystem specified.
Hello cs15lsp22ajb, you are currently logged into ieng6-202.ucsd.edu

You are using 0% CPU on this system

Cluster Status 
Hostname     Time    #Users  Load  Averages
ieng6-201   13:20:01   11  0.45,  0.35,  0.23
ieng6-202   13:20:01   7   1.19,  1.12,  1.10
ieng6-203   13:20:01   7   2.42,  2.55,  2.64


Sat Apr 09, 2022  1:24pm - Prepping cs15lsp22
[cs15lsp22ajb@ieng6-202]:~:92$ javac WhereAmI.java
[cs15lsp22ajb@ieng6-202]:~:93$ java WhereAmI
Linux
cs15lsp22ajb
/home/linux/ieng6/cs15lsp22/cs15lsp22ajb
/home/linux/ieng6/cs15lsp22/cs15lsp22ajb
[cs15lsp22ajb@ieng6-202]:~:94$
```


## 7. Setting an SSH Key :key:

#### Use ssh-keygen to create a pair of files, a public key and a private key.
On the client computer run `ssh-keygen` or `ssh-keygen -t ed25519` on windows. 

```
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
Enter passphrase (empty for no passphrase): 
Note: Make sure that you do not add a passphrase for this step.
Enter same passphrase again: 
Your identification has been saved in /Users/<user-name>/.ssh/id_rsa.
Your public key has been saved in /Users/<user-name>/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:jZaZH6fI8E2I1D35hnvGeBePQ4ELOf2Ge+G0XknoXp0 <user-name>@<system>.local
The key's randomart image is:
+---[RSA 3072]----+
|                 |
|       . . + .   |
|      . . B o .  |
|     . . B * +.. |
|      o S = *.B. |
|       = = O.*.*+|
|        + * *.BE+|
|           +.+.o |
|             ..  |
+----[SHA256]-----+
```



## 8. Optimizing Remote Running :link:

### Tips and tricks for remote running
* Adding a command in quotes at the end of an `ssh` command will run that command on the server

`$ ssh cs15lsp22zz@ieng6.ucsd.edu "ls"` -> This will run "ls" command on the server.

* You can use semicolons to run multiple commands on the same line:
`$ cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI`

* You can use the up-arrow :arrow_up: on your keyboard when in the terminal to cycle through your previously used commands. 

#### You can install VSCODE server on a remote server. This allows you to use VSCODE where you files and programs are stored and ran directly on the server

In VSCODE install Remote - SSH extensions


<p align="center">
    <img src="assets/images/vscodeExtensions.png" width = "400" alt="centered image" />
</p>

#### In VS Code, select Remote-SSH: Add New SSH Host... from the Command Palette (F1, Ctrl+Shift+P)

<p align="center">
    <img src="assets/images/sshHost.png" width = "400" alt="centered image" />
</p>

* When prompted enter the server address `ssh cs15lsp22ajb@ieng6.ucsd.edu`

#### This will install VSCODE server on the UCSD server.
Once VSCODE server has finished installing on the server go to the Remote Explorer tab on the left sidebar of VSCODE and click on
connect to host in new Window.

<p align="center">
    <img src="assets/images/remote.png" width = "400" alt="centered image" />
</p>

### Now you can use VSCODE and your files and programs will be stored and remotely ran on the UCSD server.

![image](/assets/images/vscodeRemote.png)

