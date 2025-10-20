# resumo-devops-5

## O que acontece no piperline de build no OCI DevOps?

O pipeline de build (construção) no OCI DevOps é o componente de Integração Contínua (CI) do fluxo de trabalho. Sua principal função é transformar o código-fonte em artefatos prontos para implantação.

Aqui está um resumo do que acontece em um pipeline de build do OCI DevOps e os estágios comuns envolvidos:

### 1. Início e Checkout do Código

O pipeline é iniciado (manual ou automaticamente via trigger por um commit no repositório de código) e sua primeira ação é, geralmente, o checkout do código-fonte a partir de um repositório (OCI Code Repository, GitHub, GitLab, etc.).

### 2. Estágio de Build Gerenciado (Managed Build Stage)

Este é o coração do pipeline de build, onde a maior parte do trabalho é feita.

- Instruções de Execução: O estágio Managed Build é guiado por um arquivo de especificação de build, chamado de build_spec.yaml, que você inclui no seu repositório de código.
- Ações Comuns:
   - Compilação: Compilar o código-fonte (por exemplo, Java, .NET, Node.js) em binários executáveis.
   - Teste: Executar testes de unidade e testes de integração para validar a funcionalidade e a qualidade do código.
   - Empacotamento: Criar o artefato final, como um arquivo .jar, .war, um pacote zip ou, mais comumente, uma imagem de contêiner Docker.
   - Análise de Código: Executar escaneamentos de vulnerabilidade ou análise estática (se configurado).

 ### 3. Estágio de Entrega de Artefatos (Deliver Artifacts Stage)

 Após o sucesso da construção e dos testes, o pipeline entrega o artefato final para um repositório OCI:

 - Armazenamento: O artefato (por exemplo, a imagem Docker) é enviado para o OCI Registry (OCIR) ou para o OCI Artifact Registry.
 - Definição: O artefato é definido no serviço OCI DevOps como um Artifact para que possa ser referenciado e usado pelo pipeline de implantação posteriormente.

### 4. Estágio de Controle e Integração

O pipeline de build pode ter estágios adicionais para orquestração:

## O que acontece no piperline de deployment no OCI DevOps?
