# specify the base image
FROM node:alpine 

# set the working directory to '/app' in the container. All following commands will be issued relative to this dir
WORKDIR /app
# copy over only the package.json file
COPY package.json .
# --only=prod makes sure that docker doesn't build and use our dev dependencies
RUN npm install --only=prod
# copy over all of our remaining source code 
COPY . .

# set the command to run when the container starts up
CMD ["npm", "start"]