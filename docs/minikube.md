### Key Steps to Deploy FastAPI App on Minikube

1.  **Prepare Deployment and Service YAML**:
    
    -   Ensure `deployment.yaml` and `service.yaml` files are ready.
2.  **Deploy FastAPI App**:
    
   ```bash
    `kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml` 
   ```  
    -   This applies the configuration and deploys your app to the Kubernetes cluster.
3.  **Check Pod Status**:
    
    ``` bash
    `kubectl get pods` 
     ```
    -   Verify that the FastAPI app pods are running successfully.
4.  **Expose FastAPI Using NodePort**:
    
    -   To access the app, run:
        
         ```bash
        `minikube service fastapi-service` 
        ``` 
    -   This will open the app in a browser. Alternatively, check services and manually get the NodePort:
        
        ```bash
        `kubectl get services` 
         ```
5.  **Access FastAPI Manually**:
    
    -   Access the app using the Minikube IP and NodePort:
        
         ```bash
        `http://<minikube-ip>:<node-port>` 
         ```
6.  **Troubleshoot Pods**:
    
    -   **View Pod Events**:
        
         ```bash
        `kubectl describe pod <pod-name>` 
         ```
    -   **Check Pod Logs**:
        
        ``` bash
        `kubectl logs <pod-name>` 
         ```
7.  **Use Minikube Dashboard (Optional)**:
    
    ``` bash
    `minikube dashboard` 
     ```
    -   Provides a visual interface to manage Kubernetes resources.
8.  **Rerun Deployment** (if needed):
    
    ```bash
    kubectl delete -f deployment.yaml
    kubectl apply -f deployment.yaml
    ```