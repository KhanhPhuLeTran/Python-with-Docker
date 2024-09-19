# Python-with-Docker
## Directory Structure

Ensure the `python_app` directory contains the following files:
```
python_app/
├── balanced_df.csv 
├── maxent_model.pkl 
├── stopword_train.txt 
├── teencode.xlsx 
```

## Steps to Deploy

### 1. Navigate to the python_app Directory

Open the terminal and navigate to the `python_app` directory:
```powershell
PS D:\Docker\python_app> cd D:\Docker\python_app
```

### 2. Build the Docker Image

Create a Docker image from the `Dockerfile` in the current directory:
```powershell
PS D:\Docker\python_app> docker build -t pythonapp .
```

### 3. Verify Docker Image Creation

Check if the Docker image `pythonapp` has been created:
```powershell
PS D:\Docker\python_app> docker images
```

### 4. Run a Docker Container

Create and run a Docker container from the `pythonapp` image, mapping port 7860 of the host to port 7860 of the container:
```powershell
PS D:\Docker\python_app> docker run -it -p 7860:7860 pythonapp
```

### 5. Verify Docker Container

Check if the Docker container is running:
```powershell
PS D:\Docker\python_app> docker ps
```

### 6. Access and Test the Application Locally

Open a web browser and access the application using the following URL:
```
http://localhost:7860
```
Or:
```
http://127.0.0.1:7860
```
![image](https://github.com/user-attachments/assets/cba6bcf6-6101-426f-b976-db73ca1f7051)

### 7. Access and Test the Application Publicly

If a public URL is provided, you can also access the application using the following link:
```
https://9950d45d07602283f0.gradio.live
```
Opening this link in a browser should display the application's interface.

---
