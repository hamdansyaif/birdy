# Mini Project: Flappy Bird

## Date: 5 - Dec - 2024

### Directory Structure
```
.
├── .gitignore
├── package.json
├── README.md
├── public
└── src
    ├── assets
    ├── components
        ├── Bird
        ├── Foreground
        ├── Game
        ├── Pipe
    ├── reducers
        ├── bird.js
        ├── game.js
        ├── pipe.js
        ├── index.js
    ├── App.js
    ├── index.css
    └── index.js
``` 

###Follow the steps below to set up Docker for the Birdy project.

### 1. Make a New Folder
```bash
mkdir bird
cd bird
```

### 2. Clone this Repository
```bash
git clone https://github.com/hamdansyaif/birdy.git
```

### 3. Open the Folder You Just Cloned
```bash
cd birdy
```

### 4. Create a File Named `Dockerfile` Without Any Extension
```bash
sudo nano Dockerfile
```

### 5. Type the Following Content in `Dockerfile`
```dockerfile
FROM node:16-alpine

WORKDIR /app
COPY package* .

RUN npm install

COPY . .

CMD ["npm", "start"]
```

### 6. Save the File
- Press `Ctrl + X`, then press `Y`, and hit `Enter` to save the file.

### 7. Build the Docker Image
```bash
docker build -t reactjs/birdy:1.0.0 .
```

### 8. Run the Docker Container
```bash
docker run -d -p 5000:5000 reactjs/birdy:1.0.0
```

### 9. Open the Application in Your Browser
Go to [http://localhost:5000](http://localhost:5000).
```

###Succeed you should see like this:
<div>
<img width="338" alt="Screen Shot 2022-12-29 at 5 06 29 PM" src="https://user-images.githubusercontent.com/36496209/210019678-611e9c55-03b8-4cc5-b038-2c14d08c43d4.png">
<img width="332" alt="Screen Shot 2022-12-29 at 5 06 14 PM" src="https://user-images.githubusercontent.com/36496209/210019653-93e75410-0723-43d9-91d4-c54ce82bd2fa.png">
</div>

### Set up locally use npm
- Make sure you had NodeJS already installed v16 or above.
- Clone code to your component
  - `git clone https://github.com/hamdansyaif/birdy.git`
  - `cd birdy`
- Run in cmd for install dependencies
  - `npm install`
- Start the development server
  - `npm start`
