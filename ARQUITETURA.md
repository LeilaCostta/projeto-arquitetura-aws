Arquitetura do Projeto

Cenário

O projeto considera uma pequena loja que possui um site de vendas e deseja utilizar serviços da AWS.

A loja precisa de um local para executar sua aplicação, armazenar imagens e documentos e manter os dados de clientes, produtos e pedidos.

Escolha dos serviços

Necessidade

Serviço AWS

Motivo

Executar a aplicação

Amazon EC2

Pode fornecer a máquina virtual utilizada para executar a aplicação

Guardar imagens e arquivos

Amazon S3

Serviço voltado ao armazenamento de objetos

Guardar dados estruturados

Amazon RDS

Serviço gerenciado para bancos de dados relacionais

Fluxo pensado para a arquitetura

sequenceDiagram
    participant U as Usuário
    participant E as EC2
    participant R as RDS
    participant S as S3

    U->>E: Acessa a aplicação
    E->>R: Consulta dados
    R-->>E: Retorna os dados
    E->>S: Solicita imagem ou arquivo
    S-->>E: Retorna o arquivo
    E-->>U: Exibe o resultado

Observação

Esta é a primeira versão do projeto e representa o que estou aprendendo sobre arquitetura em nuvem. A implementação prática e novos componentes serão adicionados conforme eu avançar nos estudos.
