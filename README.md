# 🛍️ Roboshop Ansible Automation

This repository contains Ansible playbooks to automate the deployment and configuration of **Stan's Robot Shop**, a microservices-based e-commerce application.

> This repository is also used for **Ansible practice**, including real-world automation tasks, service configuration, and infrastructure provisioning.

---

## 📦 Project Overview

Roboshop (Stan's Robot Shop) is a cloud-native microservices application designed to simulate a real-world e-commerce system. It includes multiple services developed in various programming languages and runs on different technology stacks.

This Ansible-based automation setup provisions all the necessary services, configures them, and ensures the end-to-end Roboshop environment is up and running efficiently.

In addition to Roboshop deployment, this repository also serves as a **practice space for various Ansible tasks**, including:

- Creating and using roles
- Writing modular and reusable playbooks
- Managing inventories and variables
- Automating infrastructure provisioning
- Service configuration and orchestration

---

## 🚀 Technologies Used in Roboshop

The Roboshop application consists of multiple services, each implemented in different technologies:

- **Frontend**: AngularJS (1.x)
- **Web Server**: Nginx
- **Backend Services**:
  - NodeJS
  - Java
  - Python
  - Golang
  - PHP (Apache)
- **Databases**:
  - MongoDB
  - MySQL
  - Redis

---

## ⚙️ What This Repo Contains

- 🔧 Ansible playbooks for provisioning all Roboshop services
- 📁 Role-based structure for modular automation
- 📂 Practice examples for various Ansible use cases
- 🔄 Idempotent automation for repeatable deployments
- 🔐 Configurable variables for host IPs, ports, and environments

---

## 🗂️ Folder Structure

```bash
Ansible-Roboshop/
├── roles/                  # Individual Ansible roles for each microservice
│   ├── frontend/
│   ├── catalogue/
│   ├── cart/
│   ├── user/
│   ├── payment/
│   ├── shipping/
│   ├── mongodb/
│   └── ...
├── inventory.ini           # Inventory file with target hosts
├── roboshop.yaml           # Master playbook to run all roles
├── vars/                   # Variable files for service configurations
└── README.md               # Project documentation
````

---

## 📋 Prerequisites

* ✅ Ansible installed (v2.9+ recommended)
* ✅ Target machines (EC2 or on-prem) with SSH access
* ✅ Inventory file configured with target host IPs

---

## 🔧 How to Use

1. **Clone the Repository**

   ```bash
   git clone https://github.com/BharathKumarReddy2103/Ansible-Roboshop.git
   cd Ansible-Roboshop
   ```

2. **Update Inventory File**
   Modify `inventory.ini` with your server IP addresses.

3. **Run the Playbook**

   ```bash
   ansible-playbook -i inventory.ini roboshop.yaml
   ```

---

## 📸 Application UI Preview

---

## 🧠 Learning Objectives

This project helps DevOps Engineers practice and learn:

* Infrastructure automation using **Ansible**
* Role-based playbook development
* Real-world microservice orchestration
* Handling service dependencies and configurations
* Debugging distributed deployments
* Creating reusable Ansible roles and tasks
* Managing Ansible inventories, variables, conditionals, and handlers

---

## 🙌 Contributing

Contributions are welcome. Feel free to open issues or submit pull requests to improve the setup or add more practice playbooks.

---

## 📜 License

This repository is for educational and practice purposes only.

---

## 🌐 Author

**Bharath Kumar Reddy**
Senior DevOps & DataOps Engineer
🔗 [LinkedIn](https://www.linkedin.com/in/bharath-kumar-reddy2103/)
📁 [GitHub Profile](https://github.com/BharathKumarReddy2103)
