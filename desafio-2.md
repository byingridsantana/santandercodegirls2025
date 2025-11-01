### Conceitos Explorados

- Aplicar os conceitos aprendidos sobre AWS Step Functions;  
- Criar e testar workflows automatizados;  
- Documentar o processo técnico de forma clara e estruturada;  
- Utilizar o GitHub como ferramenta de documentação técnica.

---

## 🧩 Etapas Realizadas

### 1. Criação da Máquina de Estados (State Machine)
- Acesse o console AWS → **Step Functions** → *Create State Machine*  
- Escolha o modelo: **Author from scratch**  
- Defina o nome da máquina de estados, por exemplo: `ProcessarArquivosWorkflow`  
- Escolha o tipo: **Standard**  
- Cole o código JSON do workflow no editor, exemplo:

```json
{
  "Comment": "Exemplo simples de Step Function com AWS Lambda",
  "StartAt": "ProcessarArquivo",
  "States": {
    "ProcessarArquivo": {
      "Type": "Task",
      "Resource": "arn:aws:lambda:REGION:ACCOUNT_ID:function:minhaFuncaoLambda",
      "Next": "Finalizado"
    },
    "Finalizado": {
      "Type": "Succeed"
    }
  }
}
