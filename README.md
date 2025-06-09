![Roboshop UI](https://raw.githubusercontent.com/BharathKumarReddy2103/Ansible-Roboshop/main/robot%20shop.png)

# Roboshop E-Commerce Microservices Deployment using Ansible (Without Roles)

This repository contains **Ansible playbooks** used to automate the deployment of the **Roboshop e-commerce application**, which follows a microservices architecture. Each service (like user, payment, cart, shipping, etc.) is deployed independently using simple, modular playbooks—without roles.

> 💼 This project mirrors the type of work I perform in my DevOps job, where I automate microservices deployments using Ansible in dev,staging,production environments.

---

## 🎯 Project Objective

- Automate the end-to-end deployment of the Roboshop application using Ansible
- Avoid complex role structure and use **direct playbooks** for each service
- Follow practical DevOps practices in a real-time environment
- Showcase service orchestration, dynamic configuration, and secure deployment workflows

---

## 🛒 What is Roboshop?

Roboshop is a cloud-native **microservices-based e-commerce application** built with components like:

- **Frontend** (Nginx)
- **Backend Services**: Catalogue, Cart, User, Payment, Shipping
- **Databases & Messaging**: MongoDB, MySQL, Redis, RabbitMQ

This project focuses on **automating the deployment** of these services using Ansible on virtual machines or cloud instances.

---

## 📚 Real-Time Ansible Concepts Demonstrated

| Concept             | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| `Playbooks`         | Simple service-based playbooks (`catalogue.yml`, `payment.yml`, etc.)       |
| `Variables`         | Reusable variables defined in `group_vars` or passed via `--extra-vars`     |
| `Templates`         | Dynamic config files using Jinja2                                           |
| `Loops`             | Iterative tasks for package installation or file operations                 |
| `Conditionals`      | Tasks executed based on custom logic or facts                               |
| `Handlers`          | Restarting services after configuration changes                             |
| `Tags`              | Selectively running parts of playbooks for faster debugging and testing     |
| `Vault`             | Managing sensitive data securely (`MYSQL_PASSWORD`, API keys, etc.)         |
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
├── group\_vars/
│   └── all.yml
├── inventory/
│   └── hosts.ini
├── templates/
│   └── nginx.conf.j2
└── README.md

````

---

## ⚙️ Sample Execution Commands

```bash
# Deploy the catalogue service
ansible-playbook -i inventory/hosts.ini playbooks/catalogue.yml

````

---

## 🌐 Real-World Scenario Simulated

* Each microservice is deployed separately and idempotently
* Configuration files are customized per service using templates
* Services are restarted automatically when changes occur (handlers)
* Static inventory file is used to target specific hosts per service

---

## 💡 Highlights

* Demonstrates **non-role-based** Ansible deployment for simplicity
* Covers **13+ microservices** and databases
* **Easy to understand** and customize for newcomers and professionals
* Closely resembles real-world DevOps automation workflows

---

## 📬 Connect with Me

If this project interests you or if you'd like to collaborate:

* [LinkedIn](https://www.linkedin.com/in/bharath-kumar-reddy2103/)
* [GitHub](https://github.com/BharathKumarReddy2103)
