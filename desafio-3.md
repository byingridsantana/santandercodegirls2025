Este projeto cria uma infraestrutura simples na AWS usando CloudFormation, com um bucket S3 e uma função Lambda que grava um arquivo dentro desse bucket.

## Recursos Criados

- `AWS::S3::Bucket`
- `AWS::IAM::Role`
- `AWS::Lambda::Function`

## Execução

1. Vá até o console da AWS → **CloudFormation**
2. Crie uma nova Stack → **Upload a template file**
3. Selecione `template.yaml`
4. Clique em **Next** → **Create Stack**
5. Após criada, teste a Lambda no console.

## Resultado Esperado

A execução da Lambda cria um arquivo `teste.txt` dentro do bucket S3.