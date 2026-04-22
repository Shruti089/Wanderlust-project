# Wanderlust - Your Ultimate Travel Blog 🌍✈️ -> End-to-End DevOps Deployment on AWS EKS
 
 📌 Overview

This project demonstrates a complete end-to-end DevOps pipeline for deploying a 3-tier MERN stack application on Kubernetes using AWS EKS.

It integrates CI/CD, security scanning, and monitoring to simulate a production-ready deployment workflow ✈ 

![Preview Image](https://github.com/krishnaacharyaa/wanderlust/assets/116620586/17ba9da6-225f-481d-87c0-5d5a010a9538)

### Project Deployment Flow:
<img src="https://github.com/DevMadhup/Wanderlust-Mega-Project/blob/main/Assets/DevSecOps%2BGitOps.gif" />

#

## Tech stack used in this project:
- Frontend: React
- Backend: Node.js  
- GitHub (Code)
- Docker (Containerization)
- Jenkins (CI)
- OWASP (Dependency check)
- SonarQube (Quality)
- Trivy (Filesystem Scan)
- ArgoCD (CD)
- Redis (Caching)
- AWS EKS (Kubernetes)
- Helm (Monitoring using grafana and prometheus)

### How pipeline will look after deployment:
- <b>CI pipeline to build and push</b>
![image](https://github.com/user-attachments/assets/20542d8b-0701-43ed-b2f8-82f8ed28d053)


> [!Important]
> Below table helps you to navigate to the particular tool installation section fast.

| Tech stack    | Installation |
| -------- | ------- |
| Jenkins Master | <a href="#Jenkins">Install and configure Jenkins</a>     |
| eksctl | <a href="#EKS">Install eksctl</a>     |
| Argocd | <a href="#Argo">Install and configure ArgoCD</a>     |
| Jenkins-Worker Setup | <a href="#Jenkins-worker">Install and configure Jenkins Worker Node</a>     |
| OWASP setup | <a href="#Owasp">Install and configure OWASP</a>     |
| SonarQube | <a href="#Sonar">Install and configure SonarQube</a>     |
| Email Notification Setup | <a href="#Mail">Email notification setup</a>     |
| Monitoring | <a href="#Monitor">Prometheus and grafana setup using helm charts</a>
| Clean Up | <a href="#Clean">Clean up</a>     |
#

### 🚀 Key Features
Automated CI/CD pipeline
Containerized MERN application
Kubernetes deployment on AWS EKS
Integrated security and vulnerability scanning
Code quality analysis
Real-time monitoring and observability

### 💡 Learnings
Hands-on experience with Kubernetes and AWS EKS
Building CI/CD pipelines using Jenkins and ArgoCD
Implementing DevSecOps practices (SAST & scanning)
Monitoring production workloads using Prometheus & Grafana

### 🎯 Conclusion

This project showcases how modern DevOps tools can be integrated to build a scalable, automated, and production-ready deployment pipeline.
                     
#
## Clean Up (most importantly , if you don't want extra aws bills. )

- <b id="Clean">Delete eks cluster</b>
```bash
eksctl delete cluster --name=wanderlust --region=us-west-1
```

#
