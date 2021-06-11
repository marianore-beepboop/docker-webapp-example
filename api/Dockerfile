# set base image (host OS)
FROM ubuntu:latest

WORKDIR /app

RUN apt update && apt upgrade -y
RUN apt install -y -q libc-dev build-essential python3-pip python3-dev

# copy the dependencies file to the working directory
COPY requirements.txt .

# install dependencies
RUN pip install -r requirements.txt

# copy the content of the local src directory to the working directory
COPY src/ .

# command to run on container start

#ENTRYPOINT [ "python3" ]

#CMD [ "wsgi.py" ]