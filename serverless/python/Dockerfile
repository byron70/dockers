FROM python:3.7

# pips
RUN pip install --upgrade pip
RUN pip install awscli

# update apt-get
RUN apt-get update -y

# install other build tools
RUN apt-get install -y --no-install-recommends \
    jq build-essential

# Install Nodejs
RUN curl -sL https://deb.nodesource.com/setup_12.x | bash -
RUN apt-get install -y nodejs
RUN npm install -g serverless

# clean up
RUN rm -rf /var/lib/apt/lists/

# change work directory
RUN mkdir -p /app
WORKDIR /app
