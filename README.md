### Season 2 Episode 2 

# My DevOps Practical Project Journey
( Code = GitHub = Jenkins = EC2 = Docker ) a simple DevOps project which will require My Codes to be pushed GitHub which will then be passed for continuous build to Jenkins and then deployed to Amazon EC2 and then to Docker for containerization

![Web 1920 – 1](https://user-images.githubusercontent.com/56154525/200328243-b2e9e5df-0655-43fd-a8bb-7b90ce919fb1.png)


in this simple DevOps Proect i pushed a simple Default template of a Dotnet Core Application into my github repository connecting it to jenkins which makes any change  
a push in the github repository trigger a build in jenkins which which then generates a Var file.
 
NOW, that var file will then be deployed into the EC2 and in the EC2 where we have a docker file which has a 
script for the script contain which will download a tomcat image from the docker hub and then copy the var file 
into the tomcat default directory and expose the port 8080


in progress, will be up in a bit wish me luck

and happy learning with me.