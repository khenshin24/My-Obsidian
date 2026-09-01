install wsl in cmd or power shell
   `wsl --install`
  open enable windows 
		  check the windows subsystem for linux


 check the virtualization is on in task manager 
		 Click cpu and check the virtualization is enable
		 

download docker  
https://hub.docker.com/r/redis/redis-stack-server

powershell and run as  administrator 1by1 

dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
dism.exe /online /enable-feature /featurename:HypervisorPlatform /all /norestart

run this to run by port 6379
docker run -d -p 6379:6379 redis/redis-stack-server:latest

stop all the docker ps 
	to stop docker stop ID
then run the  

docker ps result
3c44a1d5bc87   redis/redis-stack-server:latest   "/entrypoint.sh"   23 minutes ago   Up 23 minutes   0.0.0.0:6379->6379/tcp   cranky_benz


docker run -v ${PWD}/local-redis-stack.conf:/redis-stack.conf -p 6379:6379 redis/redis-stack-server:latest


   
   