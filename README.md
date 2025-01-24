
![WhatsApp Image 2025-01-25 at 00 25 45_e78cdfd1](https://github.com/user-attachments/assets/84cbd949-f74b-47f2-bf76-f68f13cc8bc4)

## About 
SeaWeb is a dockerised service for hosting files onto the web with ease and minimal configuration 



## Components 
* NGINX - nginx is being used to serve files over the web with routing and configuration stuff 
* DOCKER - Docker is used to provide containerised env for all the components 
* HTML , CSS , JS  - web based tech are used to build website to use 


## Working 
![WhatsApp Image 2025-01-25 at 00 16 38_2d2f8ce7](https://github.com/user-attachments/assets/a6758d42-e404-46ee-be2c-c9336b4baff3)

The setup has been implemented using docker compose init the ports are configured to 80 (default port for the nginx) , all the files inside the repo are mounted accordingy including nginx.conf file at location /etc/nginx/nginx.conf in the nginx container and other website content mounted at /etc/nginx/website/* when compose setup is run traffic from client -> host is redirected to docker container which serves the request (files which are mounted) on the same way passing from container to host to client.    


## Usecase 
This setup is useful when needed to spontaneously host some files for testing purposed or for hosting static web siles for hosting a website just like in the current case the website is hosted withit.


# Setup 
1. Install docker (prequisite)
   
3. Clone the repo
     ```bash
     git clone https://github.com/Arnav0806/seaweb.git 
     ```
     
4. Move inside the repo
   ```bash
   cd seaweb
   ```
   
5. Put the file you want to host inside the repo
   
4. Run the setup
   ```bash
   docker compose -f seaweb.yml
   ```
   
5. Test and verify by moving to browser by typing the url
   ```text
   http://localhost/FILE-PRESENT-INSIDE-THE-REPO
   ```
   
