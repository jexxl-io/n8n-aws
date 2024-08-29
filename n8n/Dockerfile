# Use the official n8n image as the base image
FROM n8nio/n8n:latest

# Switch to user root to install dependencies
USER root

# Install Python and pip
RUN apk add --update python3 py3-pip

# Copy the requirements.txt file into the Docker image and install dependencies
COPY requirements.txt /tmp/requirements.txt
RUN pip3 install --no-cache-dir -r /tmp/requirements.txt --break-system-packages && rm -f /tmp/requirements.txt

# Switch back to user node
USER node