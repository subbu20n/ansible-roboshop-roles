![Roboshop](https://github.com/subbu20n/Ansible-Roboshop/blob/main/robot%20shop.png)

# Ansible Roboshop Roles

This repository contains Ansible roles for deploying Roboshop microservices. It demonstrates real-world DevOps practices, including modular role structure, automation, configuration management, and secret handling. This repo is ideal for showcasing your skills in interviews or as a portfolio project.

---

## Table of Contents

- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Key Ansible Concepts Used](#key-ansible-concepts-used)
- [Best Practices & Security](#best-practices--security)
- [Contributing](#contributing)
- [Suggestions & Future Improvements](#suggestions--future-improvements)
- [License](#license)
- [Contact](#contact)

---

## Overview

**Roboshop** is a set of microservices that simulate an e-commerce application, used for learning and practicing DevOps concepts. This project automates the deployment of Roboshop services using Ansible, leveraging reusable roles and playbooks for scalable, maintainable infrastructure.

---

## Repository Structure

```
ansible-roboshop-roles/
├── roles/
│   ├── catalogue/
│   ├── cart/
│   ├── common
│   ├── frontend
│   ├── payment
│   ├──rabbitmq
│   ├── redis
│   ├── user/
│   ├── shipping/
│   ├── payment/
│   ├── dispatch/
│   ├── mongodb/
│   ├── mysql/
│   └── ... (other microservices)
├── playbooks/
│   └── roboshop-deploy.yml
├── inventory.ini
├── group_vars/
│   └── all.yml
├── templates/
├── vars/
├── tasks/
├── handlers/
├── files/
├── README.md
```

---

## Getting Started

### Prerequisites

- Ansible (2.9+ recommended)
- Python (3.x recommended)
- SSH access to target nodes
- Properly configured inventory file

### Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/subbu20n/ansible-roboshop-roles.git
    cd ansible-roboshop-roles
    ```
2. **Configure your inventory:**
    - Edit `inventory.ini` with your server details.

3. **Edit group variables (if needed):**
    - Customize `group_vars/all.yml` for environment-specific variables.

---

## Usage

### Deploy Specific Microservice

```bash
ansible-playbook playbooks/roboshop-deploy.yml --tags catalogue -i inventory/hosts.ini
```

### Deploy All Microservices

```bash
ansible-playbook playbooks/roboshop-deploy.yml -i inventory/hosts.ini
```

---

## Key Ansible Concepts Used

- **Roles**: Modular structure for each microservice
- **Variables**: Centralized and environment-specific configuration
- **Templates**: Jinja2 templates for config files
- **Handlers**: Service restarts and notifications
- **Loops & Tags**: Efficient and conditional task execution
- **Conditionals**: OS and environment checks
- **Error Handling**: Failures and retries
- **Crontab**: Automated scheduled jobs

---

## Best Practices & Security

- **Never commit real credentials or secrets.**  
  Use Ansible Vault for sensitive data and provide examples only.
- **Follow principle of least privilege for SSH and sudo access.**
- Modularize roles for scalability and maintainability.
- Use idempotent tasks to ensure safe re-runs.

---

## Contributing

Contributions, suggestions, and improvements are welcome.
Please see the guidelines below:

1. Fork the repository and create your feature branch.
2. Commit your changes with clear messages.
3. Open a pull request and describe your changes.
4. For major changes, open an issue first to discuss what you would like to change.

---

## Suggestions & Future Improvements

This project follows solid Ansible and DevOps practices. The following improvements are planned or being considered:

- [ ] Add repository description and LICENSE file.
- [ ] Include badges for build, license, and last commit.
- [ ] Expand README with more usage examples and troubleshooting.
- [ ] Add more screenshots of deployments and Ansible output.
- [ ] Enable Discussions and Wiki for community knowledge sharing.
- [ ] Add detailed contributing guidelines.
- [ ] Highlight further Ansible Vault usage and best practices.

Feedback and contributions are welcome.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Contact

- **LinkedIn:** [Bharath Kumar Reddy](https://www.linkedin.com/in/subbarayudu-nandyala/)
- **GitHub:** [subbu20n](https://github.com/subbu20n)

---
