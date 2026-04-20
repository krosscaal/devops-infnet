# 🚀 Guia Infnet — DevOps com Docker, Kubernetes, Prometheus e Grafana

Projeto de infraestrutura moderna utilizando **Docker**, **Kubernetes**, **Prometheus** e **Grafana**,
com pipeline de CI/CD via **GitHub Actions**.

---

## 📋 Pré-requisitos

Certifique-se de ter instalado:

| Ferramenta | Versão mínima | Instalação |
|---|---|---|
| Docker | 24+ | [docs.docker.com](https://docs.docker.com/get-docker/) |
| kubectl | 1.29+ | [kubernetes.io/docs](https://kubernetes.io/docs/tasks/tools/) |
| Minikube | 1.32+ | [minikube.sigs.k8s.io](https://minikube.sigs.k8s.io/docs/start/) |

---

## 🗂️ Estrutura do Projeto

---

## ▶️ Como Rodar a Aplicação

# 1º — Prometheus (PVC + RBAC + Deployment + Service)
    kubectl apply -f k8s/prometheus.yaml

# 2º — Aplicação, Redis e Grafana
    kubectl apply -f k8s/deploy.yaml
### 1. Iniciar o Minikube

```bash
minikube start --cpus=4 --memory=4096

```
# 3 Verificar se todos os Pods estão Running
    kubectl get pods -n default
# 4 Obter o ip do cluster
    minikube ip
# 5 Acessar a aplicação
    http://<ip>:30000
# 6 Acessar o Grafana
    http://<ip>:30001
# 7 fazer login no Grafana
    user: admin
    password: admin123
# 8 Visuzalizar as metricas
    dashboards do grafana>Infnet>Guia Infnet - Prometheus