Projeto de Arquitetura Cloud para uma Loja na AWS

Sobre o projeto
Criei este projeto para colocar em prática alguns dos conceitos de computação em nuvem e AWS que estou estudando.
O cenário escolhido foi o de uma pequena loja que possui um site de vendas e precisa levar sua estrutura para a nuvem. A proposta inicial é separar a aplicação, os arquivos e os dados de acordo com a função de cada serviço.
Este é um projeto conceitual e ainda está em desenvolvimento.

Objetivo
A ideia é criar uma arquitetura básica na AWS que permita executar a aplicação da loja, armazenar imagens e documentos e manter os dados de clientes, produtos e pedidos em um banco de dados.

Arquitetura proposta
flowchart LR
    U[Usuário] --> EC2[Amazon EC2<br/>Aplicação]
    EC2 --> RDS[Amazon RDS<br/>Banco de Dados]
    EC2 --> S3[Amazon S3<br/>Imagens e Arquivos]

Serviços escolhidos
Amazon EC2
Escolhi o Amazon EC2 para representar o servidor virtual onde a aplicação da loja seria executada.
Nesse cenário, o sistema ou site da empresa ficaria hospedado em uma instância EC2.

Amazon S3
O Amazon S3 seria utilizado para armazenar arquivos que não precisam ficar dentro do banco de dados.
Alguns exemplos são imagens dos produtos, documentos, arquivos PDF e backups de arquivos.

Amazon RDS
O Amazon RDS seria utilizado para o banco de dados relacional da aplicação.
Nele poderiam ser armazenadas informações como clientes, produtos, pedidos, preços e quantidades.
Como imaginei o funcionamento
Quando um usuário acessa a loja, ele utiliza a aplicação que está sendo executada no EC2.
Quando a aplicação precisa consultar informações sobre clientes, produtos ou pedidos, ela acessa o banco de dados no RDS.
As imagens dos produtos e outros arquivos ficam armazenados no S3.
Dessa forma, cada serviço possui uma responsabilidade dentro da arquitetura.

O que aprendi
Com este projeto consegui entender melhor a diferença entre executar uma aplicação, armazenar arquivos e armazenar dados estruturados em um banco de dados.

Também consegui relacionar três serviços da AWS com necessidades de um cenário real:
EC2 para executar a aplicação.
S3 para armazenar arquivos.
RDS para armazenar e consultar dados em um banco de dados relacional.

Próximos passos
Conforme eu avançar nos estudos, pretendo melhorar esta arquitetura e estudar como incluir controle de acesso com IAM, Security Groups, redes com VPC, monitoramento e disponibilidade.
Também pretendo fazer uma implementação prática desses serviços futuramente.

Autora
Leila Rayline Costa Cruz
Estudante de Tecnologia em Computação em Nuvem
Técnica em Informática pelo IFAM
