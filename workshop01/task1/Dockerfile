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

ENV PORT=5000
ENV INSTANCE_NAME=""
ENV INSTANCE_HASH=""

EXPOSE ${PORT}

# Command to run your application (replace with your script or entry point)
#CMD ["python3", "main.py"]
#ENTRYPOINT ["python", "main.py"]
ENTRYPOINT python main.py
CMD []

# docker build -t dockerhubaccount/python:v1.1 .
# docker container run -d -e PORT=5000 -e INSTANCE_NAME=INSTANCE_NAME -e INSTANCE_HASH=HASH -p 5000:5000 dockerhubaccount/python:v1.1