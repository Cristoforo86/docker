## Tasks ##
Create a Multi Stage Dockerfile for a React App.
You will need two stages: a build stage where you build the React App and its static content and a second stage which is needed to serve the website with a nginx web server.


## Hints: ##
- Copy the package.json and package-lock.json (if exists) into the image
- to build the static content (compiled CSS and JavaScript) you will need to run "npm run build"
- the built static content (look at ./build) needs to be copied into the second stage, so the nginx web server can serve it
- the nginx server is started by running "nginx -g daemon off"
- Add content to the .dockerignore file as you do not want to copy every file into the image