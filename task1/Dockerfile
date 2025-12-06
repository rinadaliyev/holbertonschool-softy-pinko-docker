# Use any base Linux image—Ubuntu is typical
FROM ubuntu:22.04

# Avoid interactive prompts
ENV DEBIAN_FRONTEND=noninteractive

# Install Python3 and pip3
RUN apt-get update -y && \
    apt-get install -y python3 python3-pip && \
    apt-get clean

# Fix externally managed pip environment if needed
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask with pip3 (NOT apt-get)
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy the Python Flask API into the image
COPY api.py /app/api.py

# Expose port 5252 for Flask
EXPOSE 5252

# Run the Flask app
CMD ["python3", "api.py"]

