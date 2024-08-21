# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

# TO host through EC2 instance and docker container

steps 
step 1:  create EC2 instance and allow inbound traffic to assigned port no ie, 80 

step 2 : inside the EC2 instance install docker

command : sudo apt update
command : sudo apt install docker.io -y

step 3 : clone the code repository into the Ec2 instance

step 4 : write the docker file inside the code directory or project directory
// i have written the Dockerfile above

step 5 : build the docker file
command : docker build -t "your-image-name" .

step 6 : run the image
command : docker run -d -p 80:80 "your-image-name"


step 7 : hit through url HTTP:<your-EC2-instance-ip:port>
