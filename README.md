# Projeto Final - Integração Contínua, DevOps e Computação em Nuvem

Este é o projeto final da disciplina de Integração Contínua, DevOps e Computação em Nuvem [25E1_3].

## Requisitos

Antes de iniciar, certifique-se de que os seguintes softwares estão instalados em sua máquina:

- [Docker](https://www.docker.com/get-started): Para criação e gerenciamento de contêineres.
- [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/): Ferramenta de linha de comando para interagir com o Kubernetes.
- [Minikube](https://minikube.sigs.k8s.io/docs/start/): Para executar um cluster Kubernetes local.

## Configuração e Execução

Siga os passos abaixo para configurar e executar o projeto localmente:

1. **Inicie o Minikube**:

   ```bash
   minikube start
   ```

2. **Clone este repositório**:

   ```bash
   git clone https://github.com/vicmat07/25E13.git
   ```

3. **Navegue até o diretório do projeto**:

   ```bash
   cd 25E13
   ```

4. **Implante os recursos no Kubernetes**:

   ```bash
   kubectl apply -f k8s/
   ```

   Isso aplicará todos os arquivos de configuração YAML presentes no diretório `k8s`, configurando os deployments, services e outros recursos necessários.

5. **Verifique os pods em execução**:

   ```bash
   kubectl get pods
   ```

   Aguarde até que todos os pods estejam com o status `Running`.

6. **Acesse a aplicação**:

   Se um serviço do tipo LoadBalancer foi definido, obtenha o URL de acesso com:

   ```bash
   minikube service projeto-final-service
   ```

## Observações

- Certifique-se de que o Docker e o Minikube estão em execução antes de iniciar o processo.
- Para mais detalhes sobre cada configuração, consulte os arquivos YAML no diretório `k8s`.
