# Steps to create a sample nodejs app

reference - https://www.youtube.com/watch?v=DQJNtDm5qy0

# Step 1: 
Create a project folder.
# Step 2: 
Open VSCode Terminal

![image](https://github.com/user-attachments/assets/82298283-319e-4d2f-82af-f85c05cc5bd6)

# Step 3: 
npm init -y

![image](https://github.com/user-attachments/assets/5dbfdcb5-b6f2-4268-b6cd-06552b49f31b)

# Step 4: 
package.json file will be loaded. Edit the json file 

![image](https://github.com/user-attachments/assets/9f0566dc-3517-4d1b-845b-1fab4d0852a0)

# Step 5: 
create index.json file and paste the below code from nodejs documentation

    const express = require('express')
    const app = express()
    const port = 3000
    
    app.get('/', (req, res) => {
      res.send('Hello World!')
    })
    
    app.listen(port, () => {
      console.log(`Example app listening on port ${port}`)
    })

# Step 6: 
Install npm packages. Type "npm i express" in the terminal. It will load node modules.

![image](https://github.com/user-attachments/assets/b7fee490-44ad-4545-9c67-a3db1f1f4d46)

# Step 7: 
Type node index.js in terminal. Application is listening on port 3000. Open the browser and hit the URL -> localhost:3000

![image](https://github.com/user-attachments/assets/6919b293-9b05-4c4d-9105-010007da386c)



# Steps to Dockerize the nodejs app

1. Remove the node_module package
2. Write a Dockerfile 
   
        FROM node:slim
        WORKDIR /node-app
        COPY . /node-app
        RUN npm install
        EXPOSE 3000
        CMD node index.js 
   
4. Run the 'Docker build' command to build the image of the application from the Docker file

   docker build -t madhusmita02/hey-nodejs-app:01 .

   ![image](https://github.com/user-attachments/assets/b7ddb493-ab96-4209-837c-15229e72659c)
   
5. Run the container image

   docker container run -d -p 3000:3000 madhusmita02/hey-nodejs-app:01

6. To push the image to DockerHub

    docker login -u username         -> login to docker hub by username and password

    Once Login succeeded, push image to docker hub

    docker push madhusmita02/hey-nodejs-app:01

    Refresh Docker Hub repository to view the changes

7. To pull image from Docker Hub

   docker pull madhusmita02/hey-nodejs-app:01

   

   





