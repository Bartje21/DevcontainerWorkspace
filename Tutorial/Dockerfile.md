# Dockerfile

## How to create a Dockerfile

A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image. 
Using `docker build` users can create an automated build that executes several command-line instructions in succession.

### Guidethrough

1. Create a new file named `Dockerfile` in the root of your project.
2. Add the following content to the file:

```Dockerfile
# Use the official lightweight python image
FROM python:3.10-slim

