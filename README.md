🏨 Luxora Hotel - Complete DevOps Infrastructure Project
A production-ready hotel website deployment showcasing enterprise-grade DevOps practices and automation.

(https://github.com/Shwetachaudhary63/luxore-Hotel-DevOps-project/actions/workflows/cicd.yml)

🚀 Project Overview
End-to-end DevOps implementation featuring automated deployment, container orchestration, infrastructure as code, and comprehensive monitoring for a hotel booking website.
Live Deployment: http://54.179.179.255:8080

🛠️ Technology Stack
Infrastructure & Cloud
AWS EC2 - Cloud hosting (t3.micro, ap-southeast-1)
Amazon Linux 2023 - Operating system
Terraform - Infrastructure as Code documentation
Containerization & Orchestration
Docker - Multi-container architecture (4 services)
Kubernetes - Container orchestration manifests
Docker Compose - Container management
CI/CD & Automation
GitHub Actions - Automated CI/CD pipeline
Ansible - Configuration management
Git/GitHub - Version control and collaboration
Monitoring & Observability
Prometheus - Metrics collection (Port 9090)
Grafana - Visualization dashboards (Port 3000)
Container monitoring - Real-time resource tracking
Web Server
Nginx - Web server (Alpine-based)

📊 Architecture
┌─────────────────────────────────────────────────────┐
│                   GitHub Repository                  │
│              (Source Code & Workflows)               │
└──────────────────┬──────────────────────────────────┘
                   │
                   ▼
        ┌──────────────────────┐
        │   GitHub Actions     │
        │   (CI/CD Pipeline)   │
        │  - Build & Validate  │
        │  - Automated Testing │
        └──────────┬───────────┘
                   │
                   ▼
┌──────────────────────────────────────────────────────┐
│              AWS EC2 Instance                         │
│         (ap-southeast-1 / Singapore)                  │
│                                                       │
│  ┌────────────────────────────────────────────────┐  │
│  │          Docker Containers                     │  │
│  │                                                │  │
│  │  ┌──────────┐  ┌──────────┐  ┌──────────┐   │  │
│  │  │  Nginx   │  │Prometheus│  │ Grafana  │   │  │
│  │  │  :8080   │  │  :9090   │  │  :3000   │   │  │
│  │  └──────────┘  └──────────┘  └──────────┘   │  │
│  │                                                │  │
│  │  ┌──────────┐                                 │  │
│  │  │ Jenkins  │  (Optional)                     │  │
│  │  │  :9080   │                                 │  │
│  │  └──────────┘                                 │  │
│  └────────────────────────────────────────────────┘  │
│                                                       │
│  ┌────────────────────────────────────────────────┐  │
│  │    Kubernetes Configurations                   │  │
│  │    - Deployment (2 replicas)                   │  │
│  │    - Service (NodePort)                        │  │
│  │    - Resource management                       │  │
│  └────────────────────────────────────────────────┘  │
│                                                       │
│  ┌────────────────────────────────────────────────┐  │
│  │    Ansible Automation                          │  │
│  │    - Configuration management                  │  │
│  │    - Deployment automation                     │  │
│  └────────────────────────────────────────────────┘  │
└───────────────────────────────────────────────────────┘

🔑 Key Features
✅ Automated CI/CD
Continuous Integration with GitHub Actions
Automated build and validation on every push
Docker image building and testing
Infrastructure validation checks
✅ Container Orchestration
Multi-container Docker deployment
Kubernetes-ready manifests
High availability configuration (2 replicas)
Resource limits and health checks
✅ Infrastructure as Code
Terraform documentation for AWS resources
Ansible playbooks for configuration
Version-controlled infrastructure
✅ Monitoring & Observability
Real-time metrics with Prometheus
Visual dashboards with Grafana
Container health monitoring
System resource tracking
✅ Production-Ready
Security groups configured
Proper port management
Resource optimization
Scalable architecture

📁 Project Structure
luxore-Hotel-DevOps-project/
├── .github/
│   └── workflows/
│       └── cicd.yml              # GitHub Actions CI/CD pipeline
│
├── ansible/
│   ├── ansible.cfg               # Ansible configuration
│   ├── inventory/
│   │   └── hosts                 # Inventory file
│   ├── playbooks/
│   │   └── deploy.yml            # Deployment playbook
│   └── roles/
│       ├── docker/               # Docker role
│       ├── website/              # Website deployment role
│       └── monitoring/           # Monitoring setup role
│
├── kubernetes/
│   ├── deployment.yaml           # Kubernetes deployment
│   ├── service.yaml              # Kubernetes service
│   └── README.md                 # K8s documentation
│
├── terraform-docs/
│   ├── main.tf                   # Main infrastructure
│   ├── variables.tf              # Variables
│   ├── outputs.tf                # Outputs
│   ├── provider.tf               # Provider config
│   └── README.md                 # Terraform docs
│
├── index.html                    # Website content
├── Dockerfile                    # Container image config
├── .gitignore                    # Git ignore rules
└── README.md                     # This file

🚀 Quick Start
Prerequisites
AWS Account with EC2 access
Docker installed
Git installed
GitHub account
Local Development
# Clone repository
git clone https://github.com/Shwetachaudhary63/luxore-Hotel-DevOps-project.git
cd luxore-Hotel-DevOps-project

# Build Docker image
docker build -t luxora-hotel .

# Run locally
docker run -d -p 8080:80 luxora-hotel

# Access at http://localhost:8080
Deploy to Kubernetes
# Apply Kubernetes manifests
kubectl apply -f kubernetes/

# Verify deployment
kubectl get deployments
kubectl get pods
kubectl get services

# Access application
kubectl get service luxora-hotel-service
Ansible Deployment
# Navigate to ansible directory
cd ansible/

# Run deployment playbook
ansible-playbook -i inventory/hosts playbooks/deploy.yml

# Verify deployment
ansible all -i inventory/hosts -m ping

🌐 Access Points
Service
URL
Description
Website
http://54.179.179.255:8080
Main hotel website
Grafana
http://54.179.179.255:3000
Monitoring dashboards (admin/admin123)
Prometheus
http://54.179.179.255:9090
Metrics collection
Jenkins
http://54.179.179.255:9080
CI/CD (optional)

📊 CI/CD Pipeline
The project includes automated CI/CD using GitHub Actions:
Workflow Stages
Checkout - Pull latest code from repository
Validation - Verify repository structure
Build - Create Docker images (if Dockerfile present)
Test - Run automated tests
Deploy - Ready for deployment
Triggers
Every push to main branch
Pull requests
Manual workflow dispatch
Current Status
[
�
](https://github.com/Shwetachaudhary63/luxore-Hotel-DevOps-project/actions)

🎯 DevOps Practices Demonstrated
Infrastructure
✅ Cloud deployment (AWS EC2)
✅ Infrastructure as Code (Terraform)
✅ Automated provisioning
Containerization
✅ Docker multi-container setup
✅ Container orchestration (Kubernetes)
✅ Resource optimization
Automation
✅ CI/CD pipelines (GitHub Actions)
✅ Configuration management (Ansible)
✅ Automated testing
Monitoring
✅ Metrics collection (Prometheus)
✅ Visualization (Grafana)
✅ Real-time monitoring
Best Practices
✅ Version control (Git)
✅ Documentation
✅ Security groups
✅ Resource management
✅ High availability

📈 Monitoring
Prometheus Metrics
Container resource usage
System metrics
Application health
Grafana Dashboards
Real-time visualization
Historical data
Alert configurations
Access Grafana at: http://54.179.179.255:3000
Username: admin
Password: admin123

🔧 Configuration
Environment Variables
# AWS Configuration
AWS_REGION=ap-southeast-1
INSTANCE_TYPE=t3.micro

# Docker Configuration
DOCKER_IMAGE=luxora-hotel
CONTAINER_NAME=luxure-web

# Ports
NGINX_PORT=8080
GRAFANA_PORT=3000
PROMETHEUS_PORT=9090
JENKINS_PORT=9080
Security Groups
Port 22 (SSH)
Port 80 (HTTP)
Port 443 (HTTPS)
Port 8080 (Nginx)
Port 3000 (Grafana)
Port 9080 (Jenkins)
Port 9090 (Prometheus)

📚 Documentation
Each component has detailed documentation:
Kubernetes: See kubernetes/README.md
Terraform: See terraform-docs/README.md
Ansible: Configuration in ansible/ directory
CI/CD: Workflow file at .github/workflows/cicd.yml

🤝 Contributing
Contributions welcome! Please follow these steps:
Fork the repository
Create feature branch (git checkout -b feature/AmazingFeature)
Commit changes (git commit -m 'Add AmazingFeature')
Push to branch (git push origin feature/AmazingFeature)
Open a Pull Request

📝 License
This project is for educational and portfolio purposes.
👤 Author
Shweta Chaudhary
GitHub: @Shwetachaudhary63
LinkedIn: 

🙏 Acknowledgments
AWS for cloud infrastructure
Docker for containerization
Kubernetes for orchestration
Prometheus & Grafana for monitoring
GitHub Actions for CI/CD
Open source community

📊 Project Highlights
- **DevOps Tools:** 8 integrated
- **CI/CD Status:** 4/4 workflows passing ✅
- **Containers:** 4 running 24/7
- **Cloud:** AWS EC2 (Singapore)
- **Monitoring:** Real-time with Prometheus + Grafana
- **Deployment:** Production-ready ✅

⭐ Star this repository if you found it helpful!
Built with ❤️ using DevOps best practices
