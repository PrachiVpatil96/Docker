 sudo apt install openjdk-17-jdk -y
    4  java -version
    5  sudo apt update && sudo apt upgrade -y
    6  sudo wget -O /usr/share/keyrings/jenkins-keyring.asc   https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
    7  echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]"   https://pkg.jenkins.io/debian-stable binary/ | sudo tee   /etc/apt/sources.list.d/jenkins.list > /dev/null
    8  sudo apt-get update
    9  sudo apt-get install jenkins
   10  sudo systemctl enable jenkins
   11  sudo systemctl start jenkins
   12  sudo systemctl status jenkins