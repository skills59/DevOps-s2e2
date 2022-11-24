### Season 2 Episode 2 

# My DevOps Practical Project Journey
( Code = GitHub = Jenkins = EC2 = Docker ) a simple DevOps project which will require My Codes to be pushed GitHub which will then be passed for continuous build to Jenkins and then deployed to Amazon EC2 and then to Docker for containerization

![Web 1920 – 1](https://user-images.githubusercontent.com/56154525/200328243-b2e9e5df-0655-43fd-a8bb-7b90ce919fb1.png)


in this simple DevOps Proect i pushed a simple Default template of a Dotnet Core Application into my github repository connecting it to jenkins where when any change  
or push is made in the github repository, it triggers a build in jenkins. 

NOW, im not perfect with this yet but i can already tell where its leading to, this project is in progress well see where it ends

Happy learning with me


# Project steps
1- After pushing my codes into github

2- i proceeded to lunch a linux EC2 machine on Amazon Web Services AWS

- once the machine was up and running i went into AWS systems manager, clicked on the session manager tab and launched my linus session from there

- immidiately the terminal poped up i typed the command #sudo su after which i proceeded to install docker with the command #yum install docker -y 

- and then start docker with the command #start docker service

- and then #mkdir CustomJenkins

- #cd CustomeJenkins

-#sudo nano dockerfile

- and copy paste this command which enables you to pull a jenkins image from docker hub
       
       FROM jenkins/jenkins
        # if we want to install via apt
        USER root
        RUN apt-get update && apt-get install -y libicu-dev
        # drop back to the regular jenkins user - good practice
        USER jenkins
        
- save and return and the rn the commnd #ls 

-next you build the image with the command #docker build -t dockerfile .

-once that is done you can then run this comand and start the project fully

#docker run -p 8080:8080 -p 5000:5000 -d -v jenkins_home:/var/jenkins_home dockerfile

-to confirm this you can then run #docker ps which provides you with certain details, in the details provided copy the container ID and chck docker logs with 

- #docker logs <id>
this generates a jenkis user and password which you will use to proceed to set jenkins up in the AWS EC2.

 -To do this you need to copy your mahine address and add a port 8080 e.g http://12.244.xxx.xx:8080/

3- follow steps to create the Jenkins server on the linux EC2

4 - connect my Github with jenkins

5- in Progress LOL

i will update steps here one after the other once carried out ntil project is complete



Happy learning with me.
