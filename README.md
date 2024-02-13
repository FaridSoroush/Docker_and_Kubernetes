# Flask Hello World with Docker and Kubernetes

This project demonstrates the containerization of a simple Flask application using Docker and its deployment on a local Kubernetes cluster using Minikube. It serves as an introductory guide to Docker and Kubernetes, showcasing how to build, containerize, and deploy a "Hello, World" Flask application.

## Project Overview

The Flask application is a basic web server that returns "Hello, Docker!" when accessed. This project includes steps for:

- Creating a Flask application
- Dockerizing the Flask application
- Deploying the application to Kubernetes using Minikube

## Getting Started

### Prerequisites

- Docker
- Minikube
- kubectl
- Python 3.8 or higher

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourgithubusername/flask-hello-world-docker-k8s.git
   cd flask-hello-world-docker-k8s

2. **Build the Docker image**

Make sure you're using Minikube's Docker daemon:

   ```bash
   eval $(minikube -p minikube docker-env)
   docker build -t flask-hello-world:latest .
   ```

3. **Start MiniKube**
 
   ```bash
   minikube start
   ```

4. **Deploy the application to Kubernetes**

   ```bash
   kubectl apply -f deployment.yaml
   ```
   
5. **Access the application**

Forward a local port to the deployed application:

   ```bash
   kubectl port-forward deployment/flask-hello-world 8080:5000
   ```

Visit http://localhost:8080 in your web browser to see the "Hello, Docker!" message.

### Technologies Used

- Flask: A lightweight WSGI web application framework in Python.
- Docker: A platform for developing, shipping, and running applications in containers.
- Kubernetes (Minikube): A tool for running Kubernetes locally.

### Contributing

Contributions are welcome! Please feel free to submit a pull request.

### License

This project is open source and available under the MIT License.

### Acknowledgments

- Docker documentation
- Kubernetes documentation
- Flask documentation



