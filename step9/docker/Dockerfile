FROM python:3.8-slim-buster

# set working directory
WORKDIR /usr/src/app

# copy project file
COPY requirements.txt .

# install dependencies
# install dependencies
RUN apt-get update && \
    apt-get -y install gcc mono-mcs && \
    rm -rf /var/lib/apt/lists/*
RUN pip install -r requirements.txt

# copy all project
COPY . .

# run 
CMD [ "python", "./process/app.py" ]