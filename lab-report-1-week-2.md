# CSE 12: Setting up Visual Studio Code

[LAB 1 instruction Link](https://docs.google.com/document/d/1AO6RDoJnaWxMui-UFjEa_2bbQ4qcANpbIpPuV-awsOg/edit#)

## 1. Download VScode for your operating system [VSCODE link](https://code.visualstudio.com/download) :arrow_left:
<p align="center">
    <img src="assets/images/vscodeDownload.png" width = "500" alt="centered image" />
</p>

## 2. Install VSCODE

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
    <img src="assets/images/vscodestep3.png" width = "500" alt="centered image" />
</p>


## 3. Install OpenSHH (Windows Guide)
### Open Power shell and enter command to check if Openssh is already installed
``` bat
Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'
```
<p align="center">
    <img src="assets/images/powershell1.png" width = "500" alt="centered image" />
</p>

#### If Open SSH is not installed, install it with the following powershell command:

``` cmd
# Install the OpenSSH Client
Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

# Install the OpenSSH Server
Add-WindowsCapability -Online -Name OpenSSH.Server~~~~0.0.1.0
```


## 4. Connecting to Remote Server
> #### In VScode open a terminal in VSCode (Ctrl + `, or use the Terminal → New Terminal menu option).

#### Connect to the ieng6 server using ssh
> #### Note: Replace cs15lsp22zz with your account name.

``` bash
$ ssh cs15lsp22zz@ieng6.ucsd.edu
```
#### When prompted enter you password. Your results should look simmilar to this
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
