# AWS Static Site on EC2

This project shows how to deploy a simple static website using AWS EC2.

## Architecture
 ```mermaid 
graph TD;
    GH["GitHub Repo (README and Docs)"];
    User["Your PC (Git Bash and VSCode)"];
    EC2["EC2 Instance (Amazon Linux + Apache)"];
    Browser["Public User (Browser)"];
    Mobile["Public User (Mobile Device)"];

    GH --> User;
    User -->|SSH port 22| EC2;
    EC2 -->|HTTP port 80| Browser;
    EC2 -->|HTTP port 80| Mobile;
 ```

## Steps

1. Launch EC2 (allow SSH/22 and HTTP/80 as inbound rules)
2. Install and Verify Apache running on EC2 (i.e. httpd is Active)
3. SSH into EC2 from your terminal (using your generated key while creating/launching your instance): e.g. ssh 
4. Create a test webpage on your terminal `echo 'This is a message to EC2 hosted website' | sudo tee /var/www/html/index.html`
5. Access and View the message in your web browser http://your-public-ip`
