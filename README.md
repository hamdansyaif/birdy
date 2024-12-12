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
# Install-Docker-On-Ubuntu
![image](https://github.com/user-attachments/assets/4b0b72a5-b1c1-48d3-a32a-55f1540d4b3a)

# Install Docker on Ubuntu

Follow these steps to install Docker on an Ubuntu system.

## Prerequisites

- An Ubuntu system (20.04 or later is recommended).
- A user account with `sudo` privileges.

## Steps to Install Docker

1. **Update the Package Index**
   ```bash
   sudo apt update
   ```

2. **Install Required Packages - let apt use packages over HTTPS:**
   ```bash
   sudo apt install apt-transport-https ca-certificates curl software-properties-common
   ```

3. **Add the GPG key for the official Docker repository to your system:**
   ```bash
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   ```

4. **Set Up the Docker Repository**
   This will also update our package database with the Docker packages from the newly added repo.
   ```bash
   sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
   ```

6. **Install Docker Engine**
   ```bash
   sudo apt update
   sudo apt install docker-ce
   ```

7. **Verify the Installation**
   ```bash
   sudo docker --version
   sudo docker run hello-world
   ```

   If Docker is installed successfully, the `hello-world` container will print a confirmation message.

## Optional: Manage Docker as a Non-root User

1. **Create a Docker Group**
   ```bash
   sudo groupadd docker
   ```

2. **Add Your User to the Docker Group**
   ```bash
   sudo usermod -aG docker $USER
   ```

3. **Apply Group Changes**
   Log out and log back in, or run:
   ```bash
   newgrp docker
   ```

4. **Test Non-root Access**
   ```bash
   docker run hello-world
   ```

## Uninstallation (if needed)

To remove Docker from your system, run:
```bash
sudo apt remove -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
sudo rm -rf /var/lib/docker
sudo rm -rf /var/lib/containerd
```

## References

- [Docker Documentation](https://docs.docker.com/engine/install/ubuntu/)
- [Digital Ocean - How To Install and Use Docker on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04)


### Follow the steps below to set up Docker for the Birdy project.

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

### Succeed you should see like this:
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
