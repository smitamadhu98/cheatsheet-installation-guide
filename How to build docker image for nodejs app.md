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




