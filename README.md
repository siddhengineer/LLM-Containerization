# LLM Model Finetuning and Deployment

This project involves finetuning the OLLAMA model, tweaking its parameters, and providing a GUI to interact with the model via a Streamlit web application. The project also includes DevOps tasks such as containerizing the model using Docker, pushing the Docker image to Docker Hub, creating Kubernetes deployments and services, and finally deploying and accessing the application.

## Project Structure

1. **Model Finetuning**: The OLLAMA model is finetuned and its parameters are tweaked for optimal performance.

2. **Streamlit Web Application**: A Streamlit web application is developed to provide a GUI for interacting with the finetuned model.

3. **Dockerization**: The application is containerized using Docker. The `Dockerfile` in the project root can be used to build a Docker image of the application.

4. **Kubernetes Deployment**: The Docker image is deployed to a Kubernetes cluster using a deployment configuration. A service is also created to expose the application.

## Running the Project

### Building the Docker Image

1. To build the Docker image, run the following command:

```bash
docker build -t yourusername/llm-container:llm-image .

Pushing the Docker Image to Docker Hub
To push the Docker image to Docker Hub, first tag the image with your Docker Hub username and repository, then push it:
docker tag llm-app:latest yourusername/llm-container:llm-image
docker push yourusername/llm-container:llm-image

Deploying to Kubernetes
To deploy the application to Kubernetes, apply the deployment and service configurations:
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml


Accessing the Application
The application can be accessed in two ways:

Directly via Docker: If you're running the Docker container directly, you can access the application at http://localhost:8051.

Via Kubernetes NodePort Service: If you've deployed the application to Kubernetes and exposed it via a NodePort service, you can access the application at http://localhost:30080.
```
