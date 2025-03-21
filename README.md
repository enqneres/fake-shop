# Fake Shop

# CI/CD Pipeline para Deploy Automático

Este repositório contém uma pipeline CI/CD configurada no GitHub Actions para automatizar o processo de build e deploy de uma aplicação. O processo inclui a criação de uma imagem Docker, publicação no Docker Hub e deploy no Kubernetes.

## 🚀 Funcionalidades
- **Build Docker**: Cria automaticamente a imagem Docker.
- **Publicação no Docker Hub**: Envia a imagem criada para o Docker Hub.
- **Deploy no Kubernetes**: Aplica os manifestos usando o `kubectl`.

---

## 🛠️ Pré-requisitos
Antes de começar, certifique-se de ter os seguintes itens instalados/configurados:
1. Docker instalado e configurado.
2. Conta no Docker Hub com repositório configurado.
3. Cluster Kubernetes funcionando e configurado no `kubectl`.
4. GitHub Actions habilitado no repositório.

---

## 📜 Como usar a pipeline

1. **Clone o repositório:**
   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd <NOME_DO_REPOSITORIO>

2. **Configurar as variáveis de ambiente no GitHub:**

No repositório GitHub, acesse Configurações -> Secrets e adicione:

DOCKER_USERNAME: Seu nome de usuário do Docker Hub.

DOCKER_PASSWORD: Sua senha do Docker Hub.

KUBECONFIG: Configuração do Kubernetes (se necessário).

3. **Commit e Push:**

Quando um novo commit for feito no repositório, a pipeline será acionada automaticamente.

4. **Deploy no Kubernetes:**

Acesse o cluster para verificar:
```bash
kubectl get pods
