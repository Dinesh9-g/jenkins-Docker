# jenkins

# 1.First install the jenkins.

# In ubuntu commands to install the jenkins:

 sudo apt update  */this command will update the server/*

 wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
echo "deb https://pkg.jenkins.io/debian binary/" | sudo tee /etc/apt/sources.list.d/jenkins.list

sudo apt install -y jenkins 
sudo systemctl start jenkins
sudo systemctl enable jenkins

# Docker 
 
 sudo apt install -y docker.io 
# 1. Add user to docker group
sudo usermod -aG docker $USER

# 2. Activate the change (instead of logout/login)
newgrp docker

# 3. Verify permissions
docker ps  # Should work without sudo now