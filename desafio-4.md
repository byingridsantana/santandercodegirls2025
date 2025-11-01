Este projeto faz parte do desafio da DIO para implementar uma infraestrutura automatizada na AWS utilizando o CloudFormation.  
A Stack criada provisiona uma **VPC**, uma **Sub-rede pública**, um **Security Group** e uma **instância EC2**, demonstrando o poder da infraestrutura como código (IaC).

---

## Objetivos do Desafio
- Aplicar os conceitos de **infraestrutura como código (IaC)**.  
- Automatizar a criação de recursos AWS com CloudFormation.  
- Documentar o processo técnico de forma clara e organizada.  
- Utilizar o GitHub para compartilhamento e versionamento do projeto.

---

**Componentes:**
- **VPC:** rede virtual isolada.  
- **Subnet:** sub-rede pública para hospedar a EC2.  
- **Security Group:** permite conexões SSH (porta 22) e HTTP (porta 80).  
- **EC2 Instance:** máquina virtual com Amazon Linux 2.  

---

## Como Executar

1. Acesse o console da AWS → **CloudFormation**  
2. Clique em **Create Stack** → *With new resources (standard)*  
3. Selecione **Upload a template file** e envie `template.yaml`  
4. Clique em **Next**, defina um nome (ex: `StackDesafioDIO`)  
5. Informe o nome da sua *Key Pair* (para acesso SSH)  
6. Continue clicando em **Next** até chegar em **Create stack**

Aguarde alguns minutos até a stack ser criada.  
Em seguida, vá até **EC2 → Instances** e veja sua instância em execução.

