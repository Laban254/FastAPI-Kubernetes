# FastAPI-Kubernetes
FastAPI-Kubernetes


-   **Build the Docker Image**: Open your terminal in the `fastapi-kubernetes` directory and run:
    
    ```bash
    `docker build -t  kibee254/fastapi_kubernetes:1.0 .` 
    ```
-   **Run the Docker Container**: Start the Docker container:
    
    ```bash 
    `docker run -d -p 8000:8000 fastapi-kubernetes`
    `docker push   kibee254/fastapi_kubernetes:1.0 `
    ```
