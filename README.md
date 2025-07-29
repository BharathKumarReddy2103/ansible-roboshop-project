![Roboshop UI](https://raw.githubusercontent.com/BharathKumarReddy2103/Ansible-Roboshop/main/robot%20shop.png)

# Roboshop E-Commerce Microservices Deployment using Ansible (Without Roles)

This repository contains **Ansible playbooks** used to automate the deployment of the **Roboshop e-commerce application**, which follows a microservices architecture. Each service (like user, payment, etc.) can be deployed individually.

> 💼 This project mirrors the type of work I perform in my DevOps job, where I automate microservices deployments using Ansible in dev, staging, production environments.

---

## 📝 Prerequisites

- Ansible >= 2.9
- Python >= 3.6 on the control node
- SSH access to target hosts
- (Optional) Cloud provider credentials if deploying on cloud

---

## 🚀 Getting Started

1. **Clone this repository:**
   ```bash
   git clone https://github.com/BharathKumarReddy2103/ansible-roboshop-project.git
   cd ansible-roboshop-project
   ```

2. **Edit `inventory/hosts.ini`**  
   Update the file to match your environment's hostnames/IP addresses.

3. **Configure variables:**  
   Edit `group_vars/all.yml` to set passwords, ports, and other custom settings for your environment.

4. **Run playbooks:**  
   See usage examples below.

---

## 🛒 What is Roboshop?

Roboshop is a cloud-native **microservices-based e-commerce application** built with components like:

- **Frontend** (Nginx)
- **Backend Services**: Catalogue, Cart, User, Payment, Shipping
- **Databases & Messaging**: MongoDB, MySQL, Redis, RabbitMQ

This project focuses on **automating the deployment** of these services using Ansible on virtual machines or cloud instances.

---

## 💻 Microservices Overview

| Service   | Technology | Playbook              |
|-----------|------------|-----------------------|
| Frontend  | Nginx      | nginx.yml             |
| Catalogue | NodeJS     | catalogue.yml         |
| Cart      | NodeJS     | cart.yml              |
| User      | NodeJS     | user.yml              |
| Payment   | Java       | payment.yml           |
| Shipping  | Python     | shipping.yml          |
| MongoDB   | Database   | mongodb.yml           |
| MySQL     | Database   | mysql.yml             |
| Redis     | Cache      | redis.yml             |
| RabbitMQ  | Messaging  | rabbitmq.yml          |

---

## 📚 Real-Time Ansible Concepts Demonstrated

| Concept             | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| `Playbooks`         | Simple service-based playbooks (`catalogue.yml`, `payment.yml`, etc.)       |
| `Variables`         | Reusable variables defined in `group_vars` or passed via `--extra-vars`     |
| `Loops`             | Iterative tasks for package installation or file operations                 |
| `Conditionals`      | Tasks executed based on custom logic or facts                               |
| `Handlers`          | Restarting services after configuration changes                             |
| `Tags`              | Selectively running parts of playbooks for faster debugging and testing     |
| `Crontab`           | Automating scheduled jobs like backups or health checks                     |
| `Error Handling`    | Using `ignore_errors`, `failed_when`, and validation steps                  |
| `Project Structure` | Cleanly organized files without roles—using simple and clear playbooks      |

---

## 📂 Repository Structure

```
Ansible-Roboshop/
├── playbooks/
│   ├── catalogue.yml
│   ├── cart.yml
│   ├── user.yml
│   ├── payment.yml
│   ├── shipping.yml
│   ├── mongodb.yml
│   ├── mysql.yml
│   ├── rabbitmq.yml
│   ├── redis.yml
│   ├── nginx.yml
├── group_vars/
│   └── all.yml
├── inventory/
│   └── hosts.ini
└── README.md
```

---

## ⚙️ Sample Execution Commands

```bash
# Deploy the catalogue service
ansible-playbook -i inventory/hosts.ini playbooks/catalogue.yml

# Deploy all services (example)
ansible-playbook -i inventory/hosts.ini playbooks/nginx.yml
ansible-playbook -i inventory/hosts.ini playbooks/cart.yml
# ...and so on
```

---

## 🌐 Real-World Scenario Simulated

- Each microservice is deployed separately and idempotently
- Configuration files are customized per service using templates
- Services are restarted automatically when changes occur (handlers)
- Static inventory file is used to target specific hosts per service

---

## 💡 Highlights

- Demonstrates **non-role-based** Ansible deployment for simplicity
- Covers **13+ microservices** and databases
- **Easy to understand** and customize for newcomers and professionals
- Closely resembles real-world DevOps automation workflows

---

## ❓ Troubleshooting

- **Permission denied (publickey):**  
  Ensure your SSH keys are set up and agents are running.

- **Missing dependencies:**  
  Verify Ansible and Python versions are correct on your control node.

- **Playbook errors:**  
  Check that your inventory and variables files are correctly configured.

---

## 📜 License

This repository is licensed under the MIT License.

---

## 📬 Connect with Me

If this project interests you or if you'd like to collaborate:

- [LinkedIn](https://www.linkedin.com/in/bharath-kumar-reddy2103/)
- [GitHub](https://github.com/BharathKumarReddy2103)

