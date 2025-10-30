# aws-cloudformation-lab
# Implementando sua Primeira Stack com AWS CloudFormation

## Descrição do Desafio
Este repositório foi criado para documentar o desafio “Implementando sua Primeira Stack com AWS CloudFormation”, proposto pela Digital Innovation One (DIO).  
O objetivo é aplicar os conceitos de **infraestrutura como código (IaC)** na prática, utilizando o CloudFormation para provisionar e gerenciar recursos na AWS de forma automatizada e padronizada.

---

## Objetivos de Aprendizagem
Ao concluir este desafio, eu fui capaz de:
- Entender o conceito de infraestrutura como código (IaC);
- Implementar e gerenciar uma Stack utilizando o AWS CloudFormation;
- Criar templates no formato YAML ou JSON para descrever recursos da AWS;
- Documentar e versionar configurações de infraestrutura no GitHub.

---

## O que é o AWS CloudFormation
O **AWS CloudFormation** é um serviço que permite criar e gerenciar recursos da AWS de forma automatizada, usando **templates** escritos em **YAML** ou **JSON**.  
Com ele, você define toda a sua infraestrutura — como instâncias EC2, buckets S3, tabelas DynamoDB e funções Lambda — dentro de um arquivo de configuração, e a AWS se encarrega de construir tudo conforme especificado.

Em outras palavras, o CloudFormation é como uma **“receita de bolo” da infraestrutura**:  
você escreve os ingredientes (recursos) e o modo de preparo (parâmetros e dependências), e a AWS monta tudo automaticamente.

---

## Conceitos-Chave

| Conceito | Descrição |
|-----------|------------|
| **Template** | Arquivo em YAML ou JSON que descreve os recursos a serem criados. |
| **Stack** | Conjunto de recursos criados a partir de um template. |
| **Resources** | Componentes reais da AWS (EC2, S3, VPC, etc). |
| **Parameters** | Variáveis que permitem personalizar o template. |
| **Outputs** | Informações de saída, como o ID de uma instância criada. |
| **Change Set** | Pré-visualização das mudanças antes de aplicá-las. |

---

## Exemplo de Template (YAML)

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Description: Exemplo simples de criação de um bucket S3 com CloudFormation

Resources:
  MeuBucketS3:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: meu-primeiro-bucket-cloudformation
      VersioningConfiguration:
        Status: Enabled
