# Hazran Ahmad – Personal DevOps Portfolio ⚡

**Live Demo**: http://54.205.108.244  
**GitHub Actions CI/CD**: [![CI/CD](https://github.com/kaelcloud/aws-docker-portfolio/actions/workflows/deploy.yml/badge.svg)](https://github.com/kaelcloud/aws-docker-portfolio/actions)

Personal portfolio website deployed fully automated on AWS using Docker + ECR + EC2 + GitHub Actions.

**Every push to `main` → auto build → push ECR → deploy EC2 dalam < 3 minit.**

---

### 🏗️ Architecture Diagram
![Architecture](architecture.png)
*(Simple diagram: GitHub → GitHub Actions → Build Docker → Push ECR → Pull & Run on EC2)*

### 🚀 Tech Stack
| Layer              | Technology                          |
|--------------------|-------------------------------------|
| Web Server         | Nginx (Alpine)                      |
| Container          | Docker                              |
| Registry           | Amazon ECR                          |
| Compute            | AWS EC2 (t2.micro – Free Tier)      |
| CI/CD              | GitHub Actions (self-hosted runner feel) |
| OS                 | Amazon Linux 2023                   |
| Region             | us-east-1 (N. Virginia)             |

### 🔥 Features
- Zero manual deployment
- Full CI/CD pipeline from code to production
- Dockerized static website
- Automated Docker image build & push to ECR
- Automated deployment to EC2
- Live in under 3 minutes after push

### 🛠️ How to Run Locally
```bash
git clone https://github.com/kaelcloud/aws-docker-portfolio.git
cd aws-docker-portfolio
docker build -t portfolio .
docker run -p 8080:80 portfolio
# Open http://localhost:8080
