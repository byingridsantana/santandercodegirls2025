### Conceitos Chave Explorados

* **AMI (Amazon Machine Image):** O template com o sistema operacional e softwares iniciais.
* **Tipo de Instância:** Seleção de recursos de hardware (CPU, RAM, Rede - ex: `t2.micro`).
* **Par de Chaves (Key Pair):** Necessário para a conexão SSH segura.
* **Security Groups:** O firewall virtual que controla o tráfego de entrada (Inbound) e saída (Outbound).

## Passo a Passo Prático (Minhas Anotações)

### 1. Criação da Instância EC2

* **AMI Selecionada:** [Ex: Amazon Linux 2 ou Ubuntu Server]
* **Tipo:** `t2.micro` (dentro da camada gratuita).
* **Rede:** [VPC e Subnet padrão ou personalizada].

### 2. Configuração do Security Group

* **Regras de Entrada**

    * Porta 22 (SSH): Liberada apenas para o meu IP 
    * Porta 80 (HTTP): [Se você instalou um servidor web básico, como Apache ou Nginx].

### 3. Gerenciamento do Ciclo de Vida

* **Ações Praticadas:**

    1 - Iniciei a instância.
    2 - Conectei-me via SSH usando o par de chaves
    3 - Instalei o Apache.
    4 - Parei a instância.
    5 - Reiniciei a instância.
    6 - Terminei a instância para evitar custos e finalizar o desafio.