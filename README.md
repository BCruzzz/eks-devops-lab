# 🚀 AWS EKS DevOps Lab – Terraform + Kubernetes

Este repositório contém um **laboratório prático de DevOps / Cloud** utilizando **AWS (Free Tier com ajustes conscientes)**, simulando um ambiente próximo ao **mundo real**, com foco em infraestrutura como código, Kubernetes e cloud.

O projeto foi desenvolvido com o objetivo de **ganhar experiência prática**, consolidar conceitos de **DevOps e Cloud**, e servir como **portfolio profissional no GitHub**.

---

## 📌 Resumo

Provisionamento completo de infraestrutura na AWS utilizando **Terraform**, com deploy de uma aplicação containerizada em um cluster **Amazon EKS**, exposta publicamente através de um **AWS Load Balancer**.

O laboratório cobre desde a criação da rede até o deploy e exposição da aplicação, seguindo práticas comuns de ambientes corporativos.

---

## 🧱 Arquitetura

- AWS VPC customizada
- Subnets públicas e privadas
- Internet Gateway
- Amazon EKS
- Managed Node Group
- AWS VPC CNI
- Kubernetes Deployment
- Kubernetes Service (LoadBalancer)

---

## ⚙️ Stack Utilizada

- **AWS**
- **Terraform**
- **Amazon EKS**
- **Kubernetes**
- **Docker**
- **AWS CLI**
- **kubectl**

---

## 🗂 Estrutura do Repositório

```bash
.
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   ├── vpc.tf
│   ├── eks.tf
│   └── node-group.tf
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
├── app/
│   ├── Dockerfile
│   └── index.html
└── README.md
```

---

## 🚀 Provisionamento da Infraestrutura

Inicialize o Terraform:

```bash
terraform init
```

Valide os arquivos:

```bash
terraform validate
```

Crie a infraestrutura na AWS:

```bash
terraform apply
```

---

## ☸️ Configuração do Kubernetes

Atualize o kubeconfig para acessar o cluster:

```bash
aws eks update-kubeconfig --region us-east-1 --name <nome-do-cluster>
```

Verifique o status dos nodes:

```bash
kubectl get nodes
```

---

## 📦 Deploy da Aplicação

Aplicar os manifestos Kubernetes:

```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

Verificar os Pods:

```bash
kubectl get pods
```

---

## 🌐 Acesso à Aplicação

Verifique o Service:

```bash
kubectl get svc
```

A aplicação estará acessível através do **EXTERNAL-IP** gerado pelo AWS Load Balancer.

---

## ✅ Resultado

- Infraestrutura provisionada via Terraform
- Cluster EKS operacional
- Aplicação containerizada rodando em Kubernetes
- Exposição pública via Load Balancer

---

## 🧹 Limpeza do Ambiente

Para evitar custos desnecessários:

```bash
terraform destroy
```

---

## 🎯 Objetivo do Projeto

Este laboratório foi criado com foco em:
- Prática real de DevOps e Cloud
- Infraestrutura como Código (IaC)
- Kubernetes em ambiente gerenciado
- Construção de portfolio técnico

---

> Projeto desenvolvido para fins de estudo e evolução técnica contínua.

