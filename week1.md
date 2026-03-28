# Week 1: AWS Refresh & AI-Driven Development Launch

## 🎯 Goal
Refresh foundational AWS infrastructure knowledge while gaining a significant head start in the "New AI World" using AI-native development workflows in **Cursor**.

## 💻 Project
**Infrastructure as Code (IaC) for Scholar Path** Deploy the web application: [scholar-path-web-ui](https://github.com/sarat4development-sudo/scholar-path-web-ui)

---

## 🛠 Step 1: Cursor AI Setup
*The core engine for your AI-driven development.*
- [ ] **Install Locally:** Download and install [Cursor](https://cursor.com/).
- [ ] **Account Creation:** Sign up for a free tier account.
- [ ] **AI Indexing:** Open your project folder and ensure **Repository Indexing** is enabled in settings so the AI understands your full project context.

## 🐙 Step 2: GitHub & Local Environment
- [ ] **Account:** Ensure your GitHub account is active.
- [ ] **SSH Authentication:** - Open the terminal inside Cursor (`Ctrl + ~`).
  - Setup SSH keys following [GitHub's Official Guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).
- [ ] **Clone Project:** Clone the Scholar Path repository to your local machine using the SSH link.

## 🐳 Step 3: Application Containerization
- [ ] **Docker Setup:** Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop/).
- [ ] **AI-Assisted Dockerizing:** Use **Cursor Composer (Cmd+I)** to analyze the repository and generate a production-ready `Dockerfile`.
- [ ] **Local Validation:** Build and run the image locally (`docker build` / `docker run`) to ensure the web UI loads on `localhost`.
- [ ] **Sync:** Commit and push the Docker configuration to your repository.

## ☁️ Step 4: AWS Configuration
- [ ] **Access:** Complete your account setup using the invitation for **Account: 914319167644**.
- [ ] **CLI Connectivity:** - Install the AWS CLI if not already present.
  - Run `aws configure --profile scholar-path` in the Cursor terminal to link your local environment.
- [ ] **Verify:** Run `aws sts get-caller-identity --profile scholar-path` to confirm connection.

## 🏗 Step 5: AI-Driven Infrastructure (Terraform)
*Use Cursor to generate, debug, and refine all HCL code.*
- [ ] **Container Registry:** Create an **AWS ECR** repository for your Docker images.
- [ ] **Compute:** Provision a **Kubernetes (EKS) Cluster** using the `terraform-aws-modules/eks/aws` module.
- [ ] **Networking:** - Create an **Application Load Balancer (ALB)** to route incoming traffic.
  - Setup **Route 53** records to point your domain/subdomain to the Load Balancer.
- [ ] **Deployment:** Deploy the application image to the cluster and verify the live URL.

---

## 🚀 Stretch Goals
- [ ] **CI/CD Pipeline:** Create a GitHub Actions workflow (`.github/workflows/deploy.yml`) to automate the Build → Push → Deploy cycle.
- [ ] **Environment Logic:** Implement `tfvars` for `dev` and `prod` configurations to make the infrastructure modular.
- [ ] **AI Tool Research:** Research and compare Cursor with tools like **Google Antigravity** or **Windsurf** to understand the evolution of AI Agents.

---

## Reference

| Document | Purpose |
|----------|---------|
| [Agentic development crash course](agentic-development-crash-course.md) | How to work with AI agents: scope, verification, security, and day-to-day habits. |