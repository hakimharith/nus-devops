### NUS FintechSG DevOps Course

All things about Dockers, Containers and Kubernates

### CI/CD Assignment Walkthrough

## Step 1: Create a New Git Repo

Create a new git repo on your local computer

[Guide](https://kbroman.org/github_tutorial/pages/init.html)

## Step 2: Create new React App in Repository

Go to the location of your Git Repo in your command prompt and type the following

```npx create-react-app <APP-NAME>```

## Step 3: Dockerization of React App

Create a new file and name it 'Dockerfile' and add the following text into the file

```
FROM node:alpine

WORKDIR '/app'

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]

```

[Guide](https://www.youtube.com/watch?v=O3SvhpnSZWY)
Note: Remember to add ```Expose 3000``` in the Dockerfile, this will allow us to access the container on a local browser via ```http://localhost:3000/```

## Step 4: Create Git Action to Build and Push Container to Docker Hub

## Step 5: Debug

Dicipher the error message, don't give up!




