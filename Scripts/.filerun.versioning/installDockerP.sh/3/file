apt-get -y update
#apt-get -y upgrade

# Install Docker
checkIfProgramInstalled=$(dpkg -l | grep docker-ce)
if [ -z "$checkIfProgramInstalled" ]
then
    apt install -y apt-transport-https ca-certificates curl software-properties-common
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
    apt update
    apt install -y docker-ce docker-compose
else
    echo $checkIfProgramInstalled
fi

apt-get install -y docker-compose
# Give Privileges
#groupadd docker
#usermod -aG docker $USER

# Try To Pull and Run Ubuntu
#docker run --rm -it ubuntu /bin/bash

# Fix Some Errors
#chown "$USER":"$USER" /home/"$USER"/.docker -R
#chmod g+rwx "$HOME/.docker" -R
