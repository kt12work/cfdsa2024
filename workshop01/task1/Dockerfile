# Use the official Python image from the Docker Hub
FROM python:3.8.3-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app
COPY public public
COPY templates templates

# Install any dependencies (if you have a requirements.txt)
# You can skip this step if you don't have any dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose port 5000 (or any port your app uses, for example, Flask)
EXPOSE 3000

# Command to run your application (replace with your script or entry point)
#CMD ["python3", "main.py"]
ENTRYPOINT ["python", "main.py"]