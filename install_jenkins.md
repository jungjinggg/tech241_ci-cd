# Install Jenkins on AWS EC2 instance

1) Launch EC2, ubuntu 18.04

2) Security group inbound ports: allow *ssh, http, https, 8080*

3) Update the default Ubuntu packages lists for upgrades with the following command:

```sudo apt-get update```

4) Install Java8 or above

```sudo apt-get install openjdk-11-jdk```

5) Download jenkins

```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \

  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
```  
```bash
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \

  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \

  /etc/apt/sources.list.d/jenkins.list > /dev/null
```

6) Update
```bash
sudo apt-get update
```

7) Install Jenkins
```bash
sudo apt-get install jenkins
```
8) Start Jenkins
```bash
sudo systemctl start jenkins
```
9) Enable Jenkins
```bash
sudo systemctl enable jenkins
```

10) Check status if jenkins is running and this is where the login password would be
```bash
sudo systemctl status jenkins
```

## OnJenkins
1) Install required plugins  
   1) nodejs
   2) ssh agent
   3) office 365

2)  Change node js version to 12 by going manaage jenkins -> tools -> node js version -> 12.x

3)  Add webhook to github 
    * Payload:*http://localip:8080/github-webhook/* 
    * Content type: *application/json* 
    * Trigger with push and pull.

```bash
# Command for installing Jenkins
# ssh into ec2 
ssh -i "tech241.pem" ubuntu@ec2-3-252-62-239.eu-west-1.compute.amazonaws.com
# update
sudo apt update
# install java 8 or above
sudo apt install openjdk-8-jdk
# install jenkins
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee   /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]   https://pkg.jenkins.io/debian-stable binary/ | sudo tee   /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins


sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo systemctl status jenkins

```
