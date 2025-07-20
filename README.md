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

1. Launched EC2
2. SSH from Windows (Git Bash)
3. Installed Apache
4. Pushed this to GitHub
