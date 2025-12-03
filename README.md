presentation Link : https://docs.google.com/presentation/d/1UJ1fMBqSJGmqAJyP5NmecRFSFZVNEpe0/edit?usp=drive_link&ouid=100148571708942192534&rtpof=true&sd=true
Steps to Run the Repository
Clone the repository

git clone https://github.com/AhhmedAmrr/ci-cd-demo.git
cd ci-cd-demo
Review the required environment variables

Check code and Dockerfile for any used process.env.SOMETHING.
Prepare a .env file (or note required secrets for Railway configuration).
(Optional) Run locally with Docker

Build the container:
docker build -t myapp .

Run the container (with your .env or variables):
docker run --env-file .env myapp

OR set environment variables manually:
docker run -e VAR1=value1 -e VAR2=value2 myapp

Deploy to Railway
Go to Railway and create a new project.
Connect your GitHub repository (AhhmedAmrr/ci-cd-demo).
Railway auto-detects the Dockerfile and starts the build process.
In the Railway project dashboard, set all required environment variables/secrets in the "Variables" or "Secrets" tab.
Deploy the project (Railway will build & run your container).
Access your deployed app

After deployment, Railway provides a public URL to your application.
