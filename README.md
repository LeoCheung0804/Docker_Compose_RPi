# Docker_Compose_RPi
Docker Compose for Raspberry Pi Server
 Easy Raspberry Pi Server set up for Media and Website server
 1. Install Docker on raspberry pi
 * Run the following two commands to update both the package list and the packages.
 	```
        sudo apt update
        sudo apt upgrade
	```
* Download and run the official Docker setup script by running the following command.
  ```    
	curl -sSL https://get.docker.com | sh
	```
* Add current user to docker group by using the usermod command as shown below. Change “$USER” to the current users name.
    ```    
	sudo usermod -aG docker $USER
	```		
* Check system details including the list of containers, kernel version, and docker images by running the following command.
    ```    
	sudo docker info
  	```
 2. Install the latest version of portainer using the following command.
```
      sudo docker pull portainer/portainer-ce:latest
```
 3. Start up Portainer by running the following command.
 	```
      sudo docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
	```
 4. Use the yml on Portainer UI
