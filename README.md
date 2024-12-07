# Ghost in Docker

## About the Project  
This project demonstrates how to set up and run **Ghost**, an open-source platform for publishing online content, using **Docker**. The goal of this project is to provide a portable, lightweight, and easy-to-deploy solution for running Ghost locally or on any server that supports Docker.  

Key highlights of this project include:  
- **Quick setup**: Start a fully functional Ghost development instance with minimal commands.  
- **Customizable ports**: Easily map container ports to host ports for seamless local access.  
- **Development-ready**: Ideal for testing, customizing, and exploring Ghost features.  

## About Ghost  
**Ghost** is a modern platform built for publishers, bloggers, and content creators who want a fast and user-friendly tool for managing content.  
### Key Features:  
- **Publishing made simple**: Write, edit, and publish with a clean, distraction-free editor.  
- **Subscription and payment support**: Integrates with Stripe to handle memberships and payments.  
- **Fast and lightweight**: Powered by Node.js and MySQL 8 for optimal performance.  
- **Developer-friendly**: Easily customizable and extendable with robust APIs.  

Ghost provides both frontend and admin interfaces accessible via a web browser, making it an excellent choice for anyone looking to establish an online presence quickly.  


## Learning Objectives  
By completing this project, you will:  
- Understand how to set up **Ghost** using Docker for a development environment.  
- Learn how to configure environment variables like `NODE_ENV` and `url` to customize your Ghost instance.  
- Gain experience mapping container ports to host ports for seamless local access.  
- Explore the structure and features of Ghost, including its Admin interface.  
- Understand how containerization simplifies deployment and management of web applications.  

## Prerequisites  
Before launching Ghost in Docker, ensure you have the following:  
1. **Docker Installed**:  
   - Download and install Docker from the [official website](https://www.docker.com/).  
   - Verify the installation by running `docker --version` in your terminal.  

2. **Basic Docker Knowledge**:  
   - Familiarity with Docker commands like `docker run`, `docker pull`, and `docker ps`.  

3. **System Requirements**:  
   - Minimum 1 GB of free RAM and 100 MB of storage space for the Ghost instance.  

4. **Internet Connection**:  
   - Required to pull the Ghost image from Docker Hub and access online resources.  

5. **Optional Tools**:  
   - A text editor (e.g., VS Code) for editing configuration files.  
   - A web browser to access the Ghost frontend and admin interfaces.  


## Steps to Set Up Ghost in Docker  

Follow the steps below to set up and run a development instance of Ghost using Docker:  

### 1. Pull the Ghost Docker Image  
Run the following command to download the official Ghost image from Docker Hub:  
```bash  
docker pull ghost  
```

#### 2. Start a Ghost Development Instance
To start a Ghost instance for development purposes, use the following command:
```bash  
docker run -d --name ghost -e NODE_ENV=development ghost  
```
This will:
Start a container named `ghost`.
Set the environment variable `NODE_ENV` to `development`.
Make Ghost accessible on the default port `2368`.

#### 3. Access Ghost
After running the container, you can access Ghost via:
- Frontend: `http://localhost:2368`
- Admin Interface: `http://localhost:2368/ghost`

#### 4. Customize the Port 
To make Ghost to run on a custom port, use the following command:
```bash  
docker run -d --name some-ghost -e NODE_ENV=development -e url=http://localhost:3001 -p 3001:2368 ghost  
```

This will:
Map port `3001` on the host to port `2368` in the container.
Set the `url` environment variable to `http://localhost:3001`.

Now you can access Ghost at:
- Frontend: `http://localhost:3001`
- Admin Interface: `http://localhost:3001/ghost`

#### 5. Verify the Setup
Use the following command to check the running containers:
```bash  
docker ps  
```

## Demo

## Conclusion

## Future Improvements

