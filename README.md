Travel Memory Project on AWS Cloud 

This document provides detailed technical steps for deploying the TravelMemory application backend on Amazon Web Services (AWS) using Ubuntu, Node.js, MongoDB Cloud, Nginx reverse proxy, SSL via Let’s Encrypt, AMI creation, and Application Load Balancer configuration.
Backend Deployment – Key Highlights
Technology Stack
- Backend: Node.js (Express)
- Frontend: React.js
- Database: MongoDB Atlas (Cloud)
- OS: Ubuntu on AWS EC2
- Reverse Proxy: Nginx
- SSL: Let’s Encrypt
- Load Balancer: AWS Application Load Balancer
EC2 Backend Setup
- Ubuntu t3.micro instance launched
- Security Group opened for 22, 3001, 80, 443
- OS updated and upgraded
Application Deployment
- GitHub repository cloned
- .env file created with MongoDB URI and port
- Node.js and npm installed
- Backend dependencies installed
- Application started using node index.js
Backend Validation
- Backend tested using private IP
- Verified response: 'Hello World!'
Nginx Reverse Proxy
- Nginx installed
- Reverse proxy configured (80 → 3001)
- Configuration validated and reloaded
DNS & SSL Configuration
- A record added in Namecheap
- Certbot installed
- Let’s Encrypt SSL certificate issued
- HTTPS enabled
AMI Creation
- Backend EC2 converted to AMI (Backend_AMI)
High Availability
- Second EC2 instance launched using AMI
- Backend application verified
Load Balancer Setup
- Application Load Balancer created
- HTTPS listener configured
- Target group created and instances registered
- CNAME record added in Namecheap
Final Outcome
- Secure backend (HTTPS)
- Scalable architecture
- High availability enabled

Frontend Deployment – Key Highlights
Technology Stack
- Frontend: React.js
- OS: Ubuntu on AWS EC2
- Reverse Proxy: Nginx
- SSL: Let’s Encrypt
- Load Balancer: AWS Application Load Balancer
EC2 Frontend Setup
- Ubuntu t3.micro instance launched
- Security Group opened for 22, 3000, 80, 443
- OS updated and upgraded
Application Deployment
- GitHub repository cloned
- update url.js file created in frondend location
- Node.js and npm installed
- Frondend dependencies installed
- Application started using npm start
Frontend Validation
- Frontend tested using private IP
- Verified response: Travel Website
Nginx Reverse Proxy
- Nginx installed
- Reverse proxy configured (80 → 3000)
- Configuration validated and reloaded
DNS & SSL Configuration
- A record added in Namecheap
- Certbot installed
- Let’s Encrypt SSL certificate issued
- HTTPS enabled
AMI Creation
- Frontend EC2 converted to AMI (Frontend_AMI)
High Availability
- Second EC2 instance launched using AMI
- Frontend application verified
Load Balancer Setup
- Application Load Balancer created
- HTTPS listener configured
- Target group created and instances registered
- CNAME record added in Namecheap
Final Outcome
- Secure backend (HTTPS)
- Scalable architecture
- High availability enabled

