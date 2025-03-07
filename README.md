Text Generation Tool - Instructions
========================================

Project Overview:
-----------------
This project implements a text generation service using a pretrained language model (GPT-2) from Hugging Face Transformers.
The API is built with FastAPI and is containerized with Docker for easy deployment.

Features:
---------
- Text Generation: Generate text based on a user-provided prompt
- Web Interface: Simple HTML page rendered using Jinja2 templates
- Dockerized: Run the entire service in a Docker container

Prerequisites:
--------------
- Python 3.7 or later
- Docker 
- A virtual environment tool (e.g., venv) -- Optional

Setup and Installation:
-----------------------

1. Create and Activate a Virtual Environment:
   --------------------------------------------
   It is recommended to use a virtual environment to manage dependencies
   
   a. Create a virtual environment:
   
       python3 -m venv venv

   b. Activate the virtual environment:
   
       On macOS/Linux:
           source venv/bin/activate
       On Windows:
           venv\Scripts\activate


2. Build the Docker Image:
   --------------------------
   Open a terminal in your text-generation-service directory (or make sure you are in that directory). Build the Docker image with the following command:
   
       docker build -t text-generation-service-final .

3. Run the Docker Container:
   --------------------------
   Run the container and map port 8000 from the container to port 8000 on your host:
   
       docker run -p 8000:8000 text-generation-service-final

4. Application will be available at:
    http://0.0.0.0:8000
    http://localhost:8000


Example response:
-----------------
   {
     "generated_text": "Once upon a time in a land far away, there was a mysterious forest..."
   }
