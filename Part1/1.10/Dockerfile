FROM ubuntu

WORKDIR /frontend-example-docker
#Copy the cloned frontend repo inside the container inside the current workdir (that we just made)
COPY frontend-example-docker .

#Update apt and install curl
RUN apt update && apt install -y curl
#Update PPA with the newest npm and nodejs personal package archives
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

#Update npm packages (since the server complained about some things not being updated when this was not run)
RUN npm update
#Install the packages inside the json file in workdir
RUN npm install

#Expose port 5000 because the server listens to it, have to attach the computers port to this port when running the image
EXPOSE 5000

#Make the shell run command "npm start"
CMD npm start
