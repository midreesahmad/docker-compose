# FROM python:3.9-slim
# WORKDIR /app
# COPY requirements.txt .
# RUN pip install -r requirements.txt
# COPY . .
# EXPOSE 5000
# CMD ["python3", "main.py", "--host=0.0.0.0"]

# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Copy the current directory contents into the container at /app
# COPY . /app
COPY requirements.txt .


# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

COPY . /app/

# Make port 5000 available to the world outside this container
EXPOSE 5000

# Define environment variable for Flask
ENV FLASK_APP=main.py

# Run the Flask app when the container launches
# CMD ["flask", "run", "--host=0.0.0.0"]
CMD ["python3", "main.py", "--host=0.0.0.0"]   #  trying from previous dockerfile
