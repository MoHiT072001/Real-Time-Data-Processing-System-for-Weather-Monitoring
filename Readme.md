<div align="center">

# ZeoWeather

</div>

This repository contains a full-stack project developed using the MERN stack (MongoDB, Express.js, React, and Node.js) that fetches local weather data from weather API and displays it on the dashboard. Moreover it includes following features as well :-

● Error handling for invalid rule strings or data formats (e.g., missing operators, invalid comparisons).
● Validations for attributes to be part of a catalog.


## Frontend

The frontend of this project is meticulously crafted using React, a powerful JavaScript library. It serves as the backbone of the application, handling routing and rendering of multiple sub-components, including the visually appealing dashboard page, welcoming page, and the intuitive login/register pages. These pages are thoughtfully designed utilizing a blend of HTML, CSS, and JavaScript, ensuring an engaging and seamless user experience.

To fetch data from the Weather API and interact with the MongoDB database, the project leverages the Axios library. Axios provides a convenient and efficient way to make GET/POST requests, facilitating the retrieval and manipulation of data in a secure manner. By integrating Axios, the frontend seamlessly communicates with the backend, enabling smooth data exchange between the application and external APIs.

## Backend

The backend of this project is built using Express.js and Node.js, serving as a robust bridge between the React frontend and the database. It enables seamless communication and facilitates the retrieval of weather data by leveraging Express's powerful GET/POST functionality.

For efficient data storage and management, the project utilizes a MongoDB database hosted on MongoDB Atlas. The database consists of four collections: "Active Users" for currently logged-in users and "Registered Users" for storing details of registered users like name, email, password, and city, "Daily Weather Data" to store Daily aggregates and rollups, "Hourly Weather Data" to store Hourly temperatures and others.

## Installation and Setup


# Running App

**Client-side Application**

```bash
  cd client
```

```bash
  npm install
```

```bash
  npm start
```

**Server-side Application**

```bash
  cd server
```

```bash
  npm install
```

```bash
  npm start
```
Overview
This section provides step-by-step instructions on how to deploy the application using Docker and AWS EC2 for a cloud-based deployment.

Prerequisites
Before proceeding with the deployment, ensure you have the following:

AWS EC2 instance (Ubuntu or any other Linux distribution with Docker installed)
Docker and Docker Compose installed on the EC2 instance
GitHub repository links for both applications
DockerHub account to store the Docker images
Step 1: Setup the EC2 Instance
Launch an EC2 instance:

Choose an Ubuntu AMI or any other preferred Linux distribution.
Select an instance type (e.g., t2.micro for testing).
Configure the Security Group:
Allow HTTP (port 80) and Custom TCP Rule (port 5100) for accessing the applications.
Allow SSH (port 22) for accessing the server.

Connect to the EC2 instance:

Use SSH to connect:

```bash
  ssh -i /path/to/your-key.pem ubuntu@your-ec2-public-ip
```
Step 2: Install Docker and Docker Compose
Update the package manager:
```bash
  sudo apt update
```
Install Docker:
```bash
  sudo apt install -y docker.io

```
Install Docker Compose:
```bash
  sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

```
Verify the installations:
```bash
  docker --version
docker-compose --version

```
Step 3: Clone the Repositories
Clone the repositories for both applications:
```bash
  git clone https://github.com/your-username/rule-engine-with-ast.git
git clone https://github.com/your-username/real-time-weather-monitoring.git

```
Navigate to each project directory to deploy the applications.

Step 4: Configure Docker Compose for Multi-Container Deployment
Ensure the docker-compose.yml file is correctly configured in each project directory.

Build and run the containers using Docker Compose:
```bash
  docker-compose up --build -d
```
Step 5: Verify Deployment
Access the applications:

Rule Engine: http://your-ec2-public-ip:5100
Weather Monitoring: http://your-ec2-public-ip:3000 (or configured port)
Verify the services are running using:




## Tech Stack

**Frontend:** React

**Backend:** Node, Express 

**Database:** MongoDB


## Feedback

If you have any feedback, please reach out to me at mk9355297@gmail.com
