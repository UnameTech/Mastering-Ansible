
---
---

#  **Module: Mastering Ansible – Agentless Automation for DevOps**

---

##  **Introduction**

So far, you've learned how to provision infrastructure using Terraform — an excellent declarative tool to manage infrastructure. But now, ask yourself:

- How do you install NGINX on hundreds of servers after provisioning?  
- How do you configure MySQL, deploy app code, manage SSH, update users, or secure a fleet of EC2 instances?

This is where **Ansible** shines.

Ansible is a **simple, agentless, YAML-based configuration management and automation tool** used by DevOps and SRE teams to:

- Install and configure software  
- Manage user accounts and firewalls  
- Automate app deployments  
- Enforce system states across environments

Ansible works over SSH, has a low learning curve, and integrates easily into CI/CD and GitOps workflows.

---

#  **Module Objective**

By the end of this module, you will be able to write and run Ansible playbooks to automate real-world infrastructure provisioning, application deployment, and server configuration — across environments and clouds.

---

#  Course Content

---

## Section 1 – Ansible Fundamentals

- What is Configuration Management  
- Push vs Pull model  
- Ansible vs Chef vs Puppet vs SaltStack  
- Key features of Ansible  
- How Ansible works: Control Node and Managed Nodes  
- Idempotency and YAML  

---

## Section 2 – Ansible Installation and Setup

- Control node prerequisites  
- Install Ansible on Ubuntu, CentOS, Mac  
- Create a basic lab with two remote VMs (or EC2 instances)  
- Setup passwordless SSH using SSH keys  
- Configure `ansible.cfg` and `inventory` file  
- Lab:  
  - SSH into nodes  
  - Test Ansible connection with `ansible all -m ping`  

---

## Section 3 – Ad-Hoc Commands

- Ansible command structure  
- Modules overview  
- Common modules: `ping`, `shell`, `command`, `copy`, `yum`, `apt`, `service`, `user`, `file`  
- Running ad-hoc commands against groups  
- Lab:  
  - Create users  
  - Install packages  
  - Restart services across 2+ nodes  

---

## Section 4 – Ansible Playbooks

- What is a playbook  
- Structure: Play → Task → Module  
- Anatomy of a playbook file  
- Writing your first playbook: install and start Apache  
- Lab: Create playbook and execute with `ansible-playbook`  

---

## Section 5 – Variables in Ansible

- Types of variables: playbook, inventory, extra-vars  
- Variable precedence  
- Register variables and print output  
- Lab:  
  - Create dynamic playbooks using variables  
  - Use `vars_files`, `group_vars`, `host_vars`  

---

## Section 6 – Conditionals, Loops, and Handlers

- when statements  
- Loops with `with_items` and `loop`  
- Handlers and notify  
- Lab:  
  - Install multiple packages  
  - Restart service if config changes  

---

## Section 7 – Templates and Jinja2

- What is Jinja2  
- Using templates with `.j2` files  
- Create dynamic config files  
- Use facts and variables in templates  
- Lab:  
  - Create Apache virtual host config  
  - Use template to manage NGINX or MySQL config  

---

## Section 8 – Roles in Ansible

- Why roles are important (modularity, reuse)  
- Directory structure of a role  
- `defaults`, `vars`, `handlers`, `tasks`, `files`, `templates`  
- Importing and reusing roles in playbooks  
- Lab:  
  - Create a reusable `apache` or `mysql` role  
  - Deploy app using a role  

---

## Section 9 – Ansible Vault and Secrets

- Encrypt secrets using Ansible Vault  
- Create encrypted `vars.yml` file  
- Use vault with playbooks  
- Lab:  
  - Encrypt DB password  
  - Use vault password file  
  - Decrypt on runtime  

---

## Section 10 – Inventory Management

- Static inventory: INI and YAML  
- Grouping hosts  
- Nested groups  
- Dynamic inventory with AWS EC2  
  - Use ec2.py or plugins  
- Lab:  
  - Fetch hosts dynamically  
  - Run playbook across EC2 instances with tags  

---

## Section 11 – Tags, Blocks, and Includes

- Tag tasks for selective execution  
- Block multiple tasks  
- Import or include tasks and playbooks  
- Lab:  
  - Create playbook with pre_tasks, tasks, post_tasks  
  - Run tagged tasks only  

---

## Section 12 – Ansible and GitOps

- Storing Ansible playbooks in Git  
- Versioning roles and deployments  
- CI/CD pipeline integration  
  - Jenkins + Ansible  
  - GitHub Actions + Ansible  

---

## Section 13 – Real-World Use Cases and Best Practices

- Provision and configure EC2 + Apache + App Code  
- Create a user management playbook  
- Secure SSH and firewall settings  
- Deploy a multi-tier app using roles  
- Set up cron jobs and log rotation  

---

## Section 14 – Capstone Project

**Project: Fully Automated App Stack Deployment with Ansible**

- Launch 3-tier app (Web + App + DB)  
- Use dynamic inventory with AWS  
- Separate roles for Apache, App, and MySQL  
- Secure credentials with Vault  
- Push playbooks to Git and use CI/CD pipeline to trigger deployment  

---

