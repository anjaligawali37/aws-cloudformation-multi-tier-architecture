# Commands Used

## Connect to Bastion Host

ssh -i aws_login.pem ec2-user@<Bastion-Public-IP>

---

## Connect to Private EC2

ssh -i aws_login.pem ec2-user@<Private-IP>

---

## Update Packages

sudo dnf update -y

---

## Install Apache

sudo dnf install httpd -y

---

## Start Apache

sudo systemctl start httpd

---

## Enable Apache

sudo systemctl enable httpd

---

## Verify Apache

sudo systemctl status httpd

---

## Create Web Page

echo "<h1>Welcome to Private EC2 Instance 1</h1>" | sudo tee /var/www/html/index.html

---

echo "<h1>Welcome to Private EC2 Instance 2</h1>" | sudo tee /var/www/html/index.html

---

## Test Locally

curl localhost