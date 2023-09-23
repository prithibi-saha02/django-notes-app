# Simple Notes App
This is a simple notes app built with React and Django.
Simply works to note some impt tasks or feedback to work on, however to deploy this application here we implement simple methodology of dockerizing the application to maintain system complexities and using reverse proxy or port forwarding serve the application via Nginx server. 

## Steps of implementation follow bellow 

### Requirements
1. Python 3.9
2. Node.js
3. React

## Installation
1. Clone the repository
```
git clone https://github.com/prithibi-saha02/django-notes-app.git
```
2. Install docker in system
```
sudo apt install docker.io -y
```

3. Build the app 
```
docker build -t notes-app .
```

4. Run the app
```
docker run -d -p 8000:8000 notes-app:latest
```

## Now Nginx

Install Nginx reverse proxy to make this application available

`sudo apt-get update`
`sudo apt install nginx`

Open the nginx sites-enabled directory then in default file change the location using proxy_pass of python app Ip which needs to be access via instance id only instead of directly host id.

### At last the deployment is over and the webpage will be shown below:

<img width="960" alt="django notes aap nginx" src="https://github.com/prithibi-saha02/gittutorial/assets/105097119/810b7515-e787-4573-b69f-df9d6d63c375">
