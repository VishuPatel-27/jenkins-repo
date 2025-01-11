# Use an official Python runtime as a parent image
FROM python:3.7-slim AS builder

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . .

# Install any needed packages specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Use a smaller base image for the final stage
FROM python:3.7-alpine

# Set the working directory to /app
WORKDIR /app

# Copy only the necessary files from the builder stage
COPY --from=builder /app /app

# Make port 5000 available to the world outside this container
EXPOSE 5000

ENTRYPOINT [ "python", "main.py" ]