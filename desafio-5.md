O objetivo é **automatizar a execução de uma função Lambda** sempre que um arquivo for enviado (upload) para um bucket S3.  
O projeto demonstra o uso de **eventos do S3 como gatilho (trigger)** para execução de código automatizado.

---

## Etapas Realizadas

### Criação do Bucket S3

1. Acesse o console da AWS → **S3**
2. Clique em **Create Bucket**
3. Defina um nome 
4. Mantenha as configurações padrão e crie o bucket

---

### Criação da Função Lambda

1. Acesse o console da AWS → **Lambda**
2. Clique em **Create function**
3. Selecione **Author from scratch**
4. Nome: `ProcessarUploadS3`
5. Runtime: `Python 3.12`
6. Clique em **Create Function**

Cole o seguinte código no editor:

```python
import json

def lambda_handler(event, context):
    # Obtém informações do evento S3
    bucket = event['Records'][0]['s3']['bucket']['name']
    arquivo = event['Records'][0]['s3']['object']['key']

    print(f"Novo arquivo carregado no bucket: {bucket}/{arquivo}")

    return {
        'statusCode': 200,
        'body': json.dumps(f"Processamento concluído para o arquivo: {arquivo}")
    }