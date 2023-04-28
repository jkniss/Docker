# Dockerfile for Python 3.11 image

# Build the base image
FROM python:3.11.0a1-alpine3.14

# Set the working directory
WORKDIR /usr/src/app


# Create a virtual environment
RUN python -m venv venv

# Start the virtual environment
RUN source venv/bin/activate

# Start Python  in the virtual environment
CMD [ "python" ]
