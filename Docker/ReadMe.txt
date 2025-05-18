Step 1: Open your terminal (Command Prompt, PowerShell, or )
Make sure Docker is installed and running on your computer. You can verify by running:

docker --version
Step 2: Navigate to the directory where your Dockerfile is located
For example:

cd path/to/your/project
Step 3: Build the Docker image
Run this command to build your Docker image
docker build -t myapp:latest .

Step 4: Check your built image
Run:
docker images

Step 5: Run the Docker container
Run this command to start a container from your image:
docker run -d -p 8000:8000 --name myapp-container myapp:latest

Step 6: Check if the container is running
docker ps
You should see your container myapp-container running.

Step 7: Access your app
Open your browser and go to:
http://localhost:8000

Step 8 (optional): Stop the container
If you want to stop your running container:
docker stop myapp-container

Step 9 (optional): Remove the container
docker rm myapp-container
