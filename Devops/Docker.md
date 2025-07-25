- <span style="font-size:16px; color:green;">Docker</span>:
	- Docker is a virtualization software
	- packages app with all its necessary dependencies, configurations and tools
- <span style="font-size:16px; color:green;">Kernal</span>:
	- Core of every OS
	- Interacts between software components and hardware
	![[Pasted image 20250725160632.png]]

  Docker Containers are Linux based because it was originally on Linux only 
  - <span style="font-size:16px; color:green;">Docker Images</span>:
	- Executable app Artifact
	- template that defines how a container will be realized
 - <span style="font-size:16px; color:green;">Docker Container</span>:
	- runnable instance of an image
	
	# <span style="font-size:16px; color:purple;">Commands</span>:
		1. docker image 
		//Lists all local Docker images on your system 
		
		2. docker ps
		//Shows running containers only (not stopped ones).
		
		3. docker pull name:tag
		//Downloads an image from Docker Hub or another registry.  
		
		4. docker run name:tag
		//Runs a container from the specified image.
		
		5. docker logs id
		//Shows the console output (stdout/stderr) of a container.
		
		6. docker stop id
		//Gracefully stops a running container.
		
		# 7. docker run --name -d -p port:port name:tag
		//Runs a container: With a custom name (`--name`) 
		//in detached mode (`-d`, runs in background) 
		//With port mapping (`-p`)
		
		8. docker ps -a  
		//view all containers running and stopped
		
		9. docker start id
		//Starts a stopped container (does not create a new one).
		
		10. docker buils -t name:tag .
		//Builds a Docker image from a `Dockerfile` in the current directory 
		(`.`).

- <span style="font-size:16px; color:green;">WSL2</span> (Windows Subsystem for Linux version 2) :
	- a compatibility layer that allows you to run **Linux distributions natively on Windows** (Windows 10 and 11), with real Linux kernel support.
	
- <span style="font-size:16px; color:green;">DockerFile</span> :
	- text document that contains commands to assemble an image 
	- Dockerfiles start with a parent image "<span style="font-size:16px; color:green"> base image </span>"
![[Pasted image 20250725162905.png]]