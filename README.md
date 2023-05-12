# EKS Terraform Deployment
Este projeto utiliza o Terraform para provisionar uma cluster EKS (Amazon Elastic Kubernetes Service) na AWS (Amazon Web Services). O cluster é composto por um conjunto de recursos, incluindo VPC (Amazon Virtual Private Cloud), sub-redes, grupos de segurança e nós de trabalho.

##Pré-requisitos
Antes de começar, você deve ter o seguinte:

Conta na AWS
Credenciais da AWS configuradas
Terraform instalado
Kubectl instalado
Como usar
Siga as etapas abaixo para implantar a infraestrutura do EKS na AWS.

Passo 1: Clone o repositório
```
$ git clone <URL_DO_REPOSITÓRIO>
$ cd eks-terraform-deployment

```
Passo 2: Configure as variáveis
Copie o arquivo terraform.tfvars.example para terraform.tfvars e edite as variáveis de acordo com sua configuração.

```
$ cp terraform.tfvars.example terraform.tfvars
$ vim terraform.tfvars
```
Passo 3: Execute o Terraform
```
$ terraform init
$ terraform plan
$ terraform apply

```
Passo 4: Configure o Kubectl
```
$ aws eks update-kubeconfig --name <NOME_DO_CLUSTER>

```
Passo 5: Teste o cluster
```
$ kubectl get nodes
$ kubectl get pods -A
```
Como limpar
Para excluir todos os recursos criados pelo Terraform, execute:

``
$ terraform destroy

``
Contribuindo
Sinta-se à vontade para contribuir com este projeto! Crie um fork e envie um pull request com suas melhorias.

Licença
Este projeto é licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
