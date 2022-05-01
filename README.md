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

Using the following tutorial I downloaded and ran a simple app in a Docker container: [Sample Application](https://docs.docker.com/get-started/02_our_app/)
The application was a simple application of _To-Do list_.

I downloaded the zip file of the entire repository from github link provided. After that I extracted the file contents to my system. 

I used Visual Studio Code as an editor. I then created the Dockerfile in the same directory that is "app" where package.json was loacted , which looked like this:

   <img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/Dockerfile.png" width="600" height="300" align="center">
     

I opened the terminal and ran the command :

      `docker build -t getting-started .`
      
 These steps were to app's container image.
 
 After that to start an app container, I ran the following command on my terminal : 
 
        `docker run -dp 3000:3000 getting-started`
        
  After a few seconds, I opened the web browser to [http://localhost:3000](http://localhost:3000). where I saw the app. The final output looked something like this:
  
   <img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/output_of_task.png" width="600" height="300" align="center">
   
   

### Troubleshooting

while building the app's image container,I faced the following error:
 
   <img src="https://github.com/DreamyPujara/Oracle-Excersie-UAD/blob/main/images/error%20while%20create%20an%20image%20of%20container.png" width="600" height="300" align="center">
   
 To troubleshoot it, first I rechecked the steps I followed , I checked all the commands again and then I tried reperforming them. I reread the system requirements just to be sure that everything was on point. Then I searched for similar cases on [stakeoverflow](https://stackoverflow.com/questions/64221861/an-error-failed-to-solve-with-frontend-dockerfile-v0) just to find something appropriate. I tried out some of the command changes but nothing seemed to work. Then, I mailed Vinayak Sir about the issue I was facing. I kept on finding the resolution and finally I restarted the terminal to make WSL-2 the default version by using `--set-default-version 2` command. After that i refreshed the Docker Desktop. Following by checking the _Dockerfile_ and then performing entire process afresh. I successfully completed the task after that.



## My Experience

Overall my experience was positive on working with Docker.The Documentation Guide was tailored enough with illustrations and Helps which made the entire process very much lucid to perform. Though Unlike Microsoft Manual, Docker Guide had little to no help/Troubleshooting section which can make it a little difficult for novice users.I believe more visuals and probable errors and their solutions can be added from my side to make the entire documentation to help making deploying and maintaining the applications easier. 

Apart from that, I think Docker can be used with many alternatives to deploy applications like, The Docker Azure Integration enables developers to use native Docker commands to run applications in Azure Container Instances (ACI) when building cloud-native applications etc. 


## Feedback
Help me improve this Document by providing your valuable feedback. Suggetions are welcomed to make the document more appropriate to use. Thank you very much. 



