# Oracle-Excersie-UAD

## Installation of Docker Desktop On Windows
I used this Link [Docs.Docker](https://docs.docker.com/desktop/windows/install/) for downloading the Docker Installer. I installed the Docker Desktop suitable for my Windows 10 system.

as shown in the picture, just by clicking the "Docker desktop for windows", it will start to download the .exe file.

<img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/installing%20docker%20desktop.png" width="600" height="300" align="center">

as the executable file is around 500mb, it took a while to get downloaded. Meanwhile, to fulfill the system requirements, I downloaded and installed [linux kernal update package](https://docs.microsoft.com/en-us/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package) from the docker install documentation.

It was a easy manual of 6 steps to install WSL.which is included in system requirements. Following steps: 
(picture)

1. Enable the Windows Subsystem for Linux
    * I opened PowerShell as Administrator (Start menu > PowerShell > right-click > Run as Administrator) and enter this command:
   
                        ` dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`
     
2. Check requirements for running WSL 2
    * I checked the requirements for my system which were 
       
       To update to WSL 2, it must be running Windows 10...

        For x64 systems: Version 1903 or later, with Build 18362 or later.
        For ARM64 systems: Version 2004 or later, with Build 19041 or later.
        or Windows 11.


3. Enable Virtual Machine feature
    * Before installing WSL 2, the Virtual Machine Platform optional feature must be enabled. The machine will require virtualization capabilities to use this feature.

      Open PowerShell as Administrator and run:
      
                    `dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`
                    
4. Download the Linux kernel update package
    * I download the latest package : WSL2 Linux kernel update package for x64 machines (Simply by clicking on it, the .msi file was downloaded.)


5. Set WSL 2 as your default version
    * Next, I opened PowerShell and ran this command to set WSL 2 as the default version when installing a new Linux distribution:
                   
                   `wsl --set-default-version 2`
    
6. Install your Linux distribution of choice
    * In the last step, I went on to open microsoft store and downloaded Ubuntu Linux Distribution. 
    
    (From the distribution page, simply click "Get" to download the linux distribution.)
    
    When i launched it for the first time it took some time to de-compress the files and store it on the laptop and then the next time, it took less than a second.
    

> The Microsoft manual was very much elaborate with enough illustrations and troubleshooting suggestions that it become very easy to go through the entire process.


while this part was done, the installer was downloaded. It usually gets downloaded in the _Downloads_ folder. Double clicking on the installer will start the installing process.  

after it was downloaded, I restarted the system as instructed in the manual and it was ready to go.

>Setting up the system was over and now I went ahead and started the Orientation and Setup section from the link provided.

<img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/orientation%20and%20setup.png" width="600" height="300" align="center">



## Getting Familiar with Docker Desktop
Docker created a shortcut on the desktop (otherwise it can be found from the search bar) 

double click on the application to launch docker. It starts with a tutorial where first we clone a repository then i bulid the image then run the first container and lastly save and share the image. 

The steps were pretty simple and looked like these:

1. Cloning the repository

   <img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/docker_tut_step1_clone.png" width="600" height="300" align="center">

2. To build the image

   <img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/docker_tut_step2_build.png" width="600" height="300" align="center">
   
3. Running the First Container

   <img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/docker_tut_step3_run.png" width="600" height="300" align="center">
   
4. Save and Share the Image
  
   <img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/docker_tut_step4_save%26share.png" width="600" height="300" align="center">
   

for the last step, I needed to _sign in_ to a docker account. I didn't had one so I went ahead and _signed up_ for one from the [Docker Hub](https://hub.docker.com/).

   <img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/docker%20sign%20up.png" width="600" height="300" align="center">

after confirmimg the account via the email that I had provided , i successfully completed the tutorial. Which looked like this: 

   <img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/docker_tut_successful.png" width="600" height="300" align="center">
    

## Download and Run a Simple Application in a Docker Container
Useing the following tutorial I downloaded and ran a simple app in a Docker container:

Sample Application: https://docs.docker.com/get-started/02_our_app/

I downloaded the zip file of the entire repository from github link provided. After that i extracted the file. 

i used Visual Studio Code as an editor to work with the json file. I then created the Dockerfile in the same directory that is "app" where package.json was loacted.

I opened the terminal and ran the command :

docker build -t getting-started .

here i got the error which i trobleshooted.

## My Experience
Overall my experience was positive on working with Docker.

the sample application document lacked the troubleshooting section which might make confusion for users to get to complete it. Novice users of docker might face difficulties. 



Troubleshooting section can be added.


than i ran the command on the terminal to start the app container

i sucessfully completed the task. 
