# Dockerfile

## How to create a Dockerfile

A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image.
Using `docker build` users can create an automated build that executes several command-line instructions in succession.

### Guidethrough

1. Create a new file named `Dockerfile` in the root of your project.
2. Add the following content to the file:

```Dockerfile
# Use the official lightweight python image
FROM python:3.10-slim , python:3.10-alpine, python:3.10-buster, python:3.10-slim-buster, python:3.10-slim-bullseye, python:3.10-bullseye,
python:3.10-slim-stretch, python:3.10-stretch.
# Sets the version of the image to use for the container

# Set the working directory in the container
WORKDIR /code

# Copy the current directory contents into the container at /code
COPY ./Files ./
RUN pip install --no-cache-dir -r Files.txt

COPY ./src ./src

# Make port 8000 available to the world outside this container
EXPOSE 8000

# Define environment variable
ENV NAME World

# Run app to Server
CMD ["uvicorn", "src.main:app", "--host", "0.0.0.0.", "--port", "8000", "--reload"]
# For docker server always use "0.0.0.0." as port

# Run app.py when the container launches
CMD ["python", "app.py"]
```
