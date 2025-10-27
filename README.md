# Desafio AWS CloudFormation

## Recursos Criados na Stack

| Recurso             | Serviço   | Descrição                                           |
| ------------------- | --------- | --------------------------------------------------- |
| `MeuBucketS3`       | Amazon S3 | Armazena arquivos (não gera custo se não for usado) |
| `RoleParaAplicacao` | IAM Role  | Permissão mínima para aplicações assumirem a role   |

## Diagrama de Arquitetura

```      +-----------------------+
      |    CloudFormation     |
      | (Infraestrutura como  |
      |       Código)         |
      +----------+------------+
                 |
                 v
   +-----------------------------+
   |        Template YAML        |
   | (define recursos automaticamente) |
   +-------------+---------------+
                 |
       -------------------------
       |                       |
       v                       v
   +--------+             +-----------+
   | S3     |             | IAM Role  |
   | Bucket |             | (Role)    |
   +--------+             +-----------+
```



O diagrama acima representa como o CloudFormation utiliza o template YAML para criar automaticamente:
- Um bucket S3, responsável por armazenar dados.
- Uma IAM Role, permitindo que serviços possam assumir permissões específicas.
- Fiz esse exemplo pois não consegui baixar os arquivos que estavam na página do desafio de projeto.

