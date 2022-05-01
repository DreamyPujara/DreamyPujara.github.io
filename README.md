# Oracle-Excersie-UAD

## Installation of Docker Desktop On Windows
I used this Link [Docs.Docker](https://docs.docker.com/desktop/windows/install/) for downloading the Docker Installer. I installed the Docker Desktop suitable for my Windows 10 system.

as shown in the picture, just by clicking the "Docker desktop for windows", it will start to download the .exe file.
![image](

as the executable file is around 500mb, it took a while to get downloaded. Meanwhile, to fulfill the system requirements, I downloaded and installed linux kernal update package from the docker install documentation.

It was a easy manual of 6 steps to install WSL.which is included in system requirements. Following steps: 
(picture)

1. Enable the Windows Subsystem for Linux
2. Check requirements for running WSL 2
3. Enable Virtual Machine feature
4. Download the Linux kernel update package
5. Set WSL 2 as your default version
6. Install your Linux distribution of choice

while this part was done, the installer was downloaded. It usually gets downloaded in the download folder. Double clicking on the installer will start the installing process. 

As the system only had one option WSL 2 and not Hyper-V , so there was not any selection while running the installer. 

after it is downloaded, I restarted the system and it was ready to go.

## Getting Familiar with Docker Desktop
Docker created a shortcut on the desktop (otherwise it can be found from the search bar) 

double click on the application to launch docker. It starts with a tutorial where first we clone a repository then i bulid the image then run the first container and lastly save and share the image. 

for the last step we need to sign in to docker account. I didnt had one so i went ahead and signed up for one from the website (link). after confirnimg the account via the email address i gave, i successfully completed the tutorial. 

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
