# CS3219 - Assignment A (Using Nginx as reverse proxy in docker)

This is a repository for CS3219 assignment A - deploying a simple web server using NGINX in docker container.

There are two web applications running in their own docker container and one container for Nginx which serves as the reverse proxy.

Nginx receives the incoming request from the user and directed to the relevant web applications: website1 or website2 through port 80. 

Instructions on how to run the docker containers:
1)	Clone the code from the github repository.
2)	Go to the website 1 folder from root directory by using (cd website1) in the command prompt.
3)	Build the image for website1 by using (docker-compose build) in the command prompt.
4)	Run the docker container for website 1 by using (docker-compose up -d) in the command prompt.
5)	Next, repeat step 3 to 4 for both website2 and the proxy server after changing the directory to their respective folders by cd ../website2 and cd ../proxy respectively.
(Note: You must do for website2 and website 1 first before doing for proxy server as proxy server run on network website2_default and website1_default which is only created when you run the website2 and website1 containers)
6)	Go to browser and key in http://localhost/website1 to access to website 1 html page and key in http://localhost/website2 to access to website 2 html page. Do note that if you key in other directory include http://localhost/ , it will show an error page.

