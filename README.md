<div align="center">

```
██████╗ ███████╗██╗   ██╗ ██████╗ ██████╗ ███████╗
██╔══██╗██╔════╝██║   ██║██╔═══██╗██╔══██╗██╔════╝
██║  ██║█████╗  ██║   ██║██║   ██║██████╔╝███████╗
██║  ██║██╔══╝  ╚██╗ ██╔╝██║   ██║██╔═══╝ ╚════██║
██████╔╝███████╗ ╚████╔╝ ╚██████╔╝██║     ███████║
╚═════╝ ╚══════╝  ╚═══╝   ╚═════╝ ╚═╝     ╚══════╝
```

# 🚀 DevOps Learning Blocks

**A structured, beginner-friendly DevOps learning repository**  
*Learn → Practice → Document → Share*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Made with ❤️](https://img.shields.io/badge/Made%20with-%E2%9D%A4%EF%B8%8F-red.svg)](https://github.com)
[![DevOps Journey](https://img.shields.io/badge/Status-In%20Progress-yellow.svg)](https://github.com)

</div>

---

## 📖 About This Repository

> *"Instead of jumping directly into advanced tools, this repository follows a step-by-step path — covering fundamentals first, tools second."*

This is a **structured collection of notes, examples, and hands-on materials** built during an active DevOps learning journey. Every topic focuses on **understanding concepts first**, followed by practical implementation and real-world usage.

Whether you're a student, a developer transitioning into DevOps, or just curious — this repo is for you.

---

## 🗺️ Learning Roadmap

```
[▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓] DevOps Path
 01        02        03       04        05
Linux → Network → Git/GitHub → Shell → Docker → ...
```

---

### 01 · 🐧 Linux Fundamentals

> *The foundation everything else is built on.*

| Topic | Description |
|-------|-------------|
| 📁 File System | Navigate the Linux directory tree |
| ⌨️ Essential Commands | `ls`, `cd`, `grep`, `find`, `chmod` and more |
| 👤 User & Permissions | Manage users, groups, and file permissions |
| ⚙️ Process Management | `ps`, `top`, `kill`, background/foreground jobs |
| 📦 Package Management | `apt`, `yum`, `snap` — installing and updating software |
| 🌐 Shell Environment | `.bashrc`, environment variables, PATH |

---

### 02 · 🌐 Networking for DevOps

> *Understand how servers, clouds, and services actually talk to each other.*

| Topic | Description |
|-------|-------------|
| 🔗 OSI & TCP/IP Models | How network communication layers work |
| 🏠 IP Addressing | IPv4, IPv6, subnetting, CIDR notation |
| 🔍 DNS | Domain resolution, records, and lookups |
| 🔒 HTTP/HTTPS | How the web communicates securely |
| 🛡️ SSH | Secure remote access and key-based auth |
| 🔌 Ports & Protocols | Common ports every DevOps engineer must know |
| 🛠️ Troubleshooting | `ping`, `traceroute`, `netstat`, `curl`, `nmap` |

---

### 03 · 🌿 Git & GitHub

> *Version control is the backbone of collaborative development.*

| Topic | Description |
|-------|-------------|
| 📝 Git Basics | `init`, `add`, `commit`, `push`, `pull` |
| 🌿 Branching & Merging | Feature branches, `merge`, `rebase` |
| 🔁 Pull Requests | Code reviews and collaborative workflows |
| ⚡ Conflict Resolution | Handling merge conflicts gracefully |
| 🔄 Git Workflows | GitFlow, trunk-based development |
| 🗂️ Repo Management | Tags, releases, `.gitignore`, and best practices |

---

### 04 · 🖥️ Shell Scripting

> *Automate the boring stuff — let scripts do the heavy lifting.*

```bash
#!/bin/bash
# Your automation starts here
for task in "deploy" "monitor" "backup"; do
    echo "✅ Automating: $task"
done
```

**Topics covered:** Variables · Loops · Conditionals · Functions · I/O Handling · Automation Scripts

---

### 05 · 🐳 Docker

> *Ship your application anywhere, exactly as it runs on your machine.*

```dockerfile
FROM ubuntu:22.04
# Build once. Run anywhere.
```

| Topic | Description |
|-------|-------------|
| 🏗️ Architecture | Docker daemon, client, and registry |
| 📦 Images & Containers | Building, tagging, and running containers |
| 📄 Dockerfile | Writing efficient, layered builds |
| 💾 Volumes | Persistent data in a containerized world |
| 🔗 Networking | Container-to-container communication |
| 🎼 Docker Compose | Multi-container application management |

---

### 06 · ⚙️ GitHub Actions

> *CI/CD built directly into your repository.*

```yaml
name: Deploy Pipeline
on: [push]
jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3
```

**Topics covered:** Workflow Creation · Jobs & Steps · Runners · Secrets Management · Automated Testing · Deployment Pipelines

---

### 07 · 🔧 Jenkins

> *The battle-tested CI/CD automation server.*

| Topic | Description |
|-------|-------------|
| 🚀 Setup | Installation and initial configuration |
| 🛣️ Pipelines | Declarative and scripted pipelines |
| 🤖 Agents & Nodes | Distributed build environments |
| 🔨 Build Automation | Triggering, scheduling, and chaining builds |
| 🔌 Integrations | Connecting Jenkins with GitHub, Docker, and more |
| 🚢 Deployment Workflows | End-to-end release automation |

---

### 08 · ☸️ Kubernetes (K8s)

> *Orchestrate containers at scale — self-healing, auto-scaling, production-grade.*

```
┌─────────────────────────────────────────┐
│              Kubernetes Cluster          │
│  ┌──────────┐  ┌──────────┐  ┌───────┐  │
│  │  Pod 🟢  │  │  Pod 🟢  │  │ Pod 🟡│  │
│  └──────────┘  └──────────┘  └───────┘  │
│         Service ──▶ Ingress             │
└─────────────────────────────────────────┘
```

**Topics covered:** Pods · Deployments · Services · ConfigMaps · Secrets · Ingress · Scaling & Self-Healing

---

### 09 · 🏗️ Terraform

> *Define your infrastructure in code. Version it. Automate it. Repeat it.*

```hcl
resource "aws_instance" "web" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"
  # Infrastructure. As. Code.
}
```

**Topics covered:** Terraform Basics · Providers · Resources · Variables · State Management · Infrastructure Provisioning

---

### 10 · 🤖 Ansible

> *Agentless automation — configure servers at scale without touching each one manually.*

```yaml
- name: Configure web servers
  hosts: all
  tasks:
    - name: Install nginx
      apt:
        name: nginx
        state: present
```

**Topics covered:** Inventory · Playbooks · Roles · Variables · Templates · Server Provisioning & Automation

---

## 🎯 Who Is This For?

```
👩‍💻  Students learning DevOps from scratch
🔄  Developers transitioning into DevOps roles  
⚙️  Engineers exploring CI/CD and automation
📚  Anyone who learns best through structured resources
```

---

## 💡 Learning Philosophy

<div align="center">

```
┌──────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐
│  LEARN   │───▶│ PRACTICE │───▶│ DOCUMENT │───▶│  SHARE   │
└──────────┘    └──────────┘    └──────────┘    └──────────┘
```

*Understanding concepts first. Implementation second. Sharing always.*

</div>

---

## 📂 Repository Structure

```
devops-learning-blocks/
├── 01-linux/
│   ├── notes.md
│   └── exercises/
├── 02-networking/
├── 03-git-github/
├── 04-shell-scripting/
├── 05-docker/
├── 06-github-actions/
├── 07-jenkins/
├── 08-kubernetes/
├── 09-terraform/
└── 10-ansible/
```

---

## 🤝 Contributing

Found a mistake? Have a better explanation? Contributions are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b improve/topic-name`)
3. Commit your changes (`git commit -m 'Improve explanation for X'`)
4. Push to the branch (`git push origin improve/topic-name`)
5. Open a Pull Request

---

<div align="center">

**Happy Learning! 🚀**

*If this repository helps you, consider giving it a ⭐ — it keeps the motivation going!*

---

*Built with curiosity, documented with care.*

</div>
