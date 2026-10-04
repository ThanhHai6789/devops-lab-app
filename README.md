# Automated CI/CD Pipeline with GitHub Actions & Docker

A hands-on DevOps project demonstrating automated containerization and continuous integration (CI) using **GitHub Actions** and **Docker**.

---

##  Architecture & Tech Stack

* **Version Control:** GitHub
* **CI/CD Automation:** GitHub Actions (`.github/workflows`)
* **Containerization:** Docker
* **Application:** Web Application (`index.html` served via Nginx)

---

##  Pipeline Overview

```text
[ Developer Commit / Push ] ──► [ GitHub Actions Workflow ]
                                           │
                                           ├──► 1. Lint & Validate Code
                                           ├──► 2. Build Docker Image
                                           └──► 3. Push Image to Registry
📁 Repository Structure
Plaintext
.
├── .github/
│   └── workflows/      # GitHub Actions CI/CD workflow configurations
├── Dockerfile          # Docker container build instructions
└── index.html          # Frontend web application source
 Key Features & Highlights
Automated Builds: GitHub Actions automatically triggers a build pipeline whenever new code is pushed to the repository.

Dockerization: Standardized container environment using lightweight base images.

CI Best Practices: Clean separation of source code, container definitions, and automation pipelines.

 How to Run Locally
Clone the repository:

Bash
git clone [https://github.com/ThanhHai6789/devops-lab-app.git](https://github.com/ThanhHai6789/devops-lab-app.git)
cd devops-lab-app
Build the Docker Image:

Bash
docker build -t devops-lab-app .
Run the Container:

Bash
docker run -d -p 8080:80 devops-lab-app
Access the web app at http://localhost:8080.
