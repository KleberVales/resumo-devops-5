# resumo-devops-5

## O que acontece no piperline de build no OCI DevOps?

O pipeline de build (construção) no OCI DevOps é o componente de Integração Contínua (CI) do fluxo de trabalho. Sua principal função é transformar o código-fonte em artefatos prontos para implantação.

Aqui está um resumo do que acontece em um pipeline de build do OCI DevOps e os estágios comuns envolvidos:

### 1. Início e Checkout do Código

O pipeline é iniciado (manual ou automaticamente via trigger por um commit no repositório de código) e sua primeira ação é, geralmente, o checkout do código-fonte a partir de um repositório (OCI Code Repository, GitHub, GitLab, etc.).

### 2. Estágio de Build Gerenciado (Managed Build Stage)

Este é o coração do pipeline de build, onde a maior parte do trabalho é feita.

## O que acontece no piperline de deployment no OCI DevOps?
