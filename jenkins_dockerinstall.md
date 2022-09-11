**Jenkins in Docker Windows**

This is a description of installing in Docker Jenkins and use it as a test playfield by saving to local hdd configuration data.

Steps in installation:
	
	1.	Install Docker Community Edition
	2.	Install Docker container for jenkins from DockerHub
>         docker run -d -p 8080:8080 -v C:\Users\crazyT\jenkins:/var/jenkins_home jenkins/jenkins

        -p : PortMapping
        -d : run in Background
        -v : define static folder where files can be saved on docker host to be used for further jenkins container deployments        
                dockerhost:dockercontainer path
        -u : user
	3.	Read Jenkins password from the container
>         docker exec 0223b0e8cc17 cat /var/jenkins_home/secrets/initialAdminPassword
        read container  : docker ps command
	4.	Go to HostIP:8080 to configure Jenkins as wished
	
Now you have a docker container configured and up and running to test Jenkins