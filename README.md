## Capítulo 1 | Configurações e teste inicial com S3

### Criando e acessando conta 

1. Criei uma conta mãe (luizhsou1), mas não deve se usar ela para fazer dev ou alguma, pois ela tem acesso a tudo
2. Procura um serviço chamado IAM, que é o serviço para gerenciar acessos na AWS
3. Crio um grupo admin e dou permissão de admininistratorAccess para ele, e add esse user
4. Baixa o arquivo de credenciais gerado, desloga do usuário anterior e clica no link gerado, informando as coisas que faltam, accountId já vem preenchido
5. Linkar minha conta da AWS, as configurações locais da máquina
6. Baixar AWS CLI caso não tenha
7. $ aws configure (fornecendo as credenciais de acesso)
8. $ aws s3 ls (Verificar bucket que está na AWS)
9. $ echo "Hello World" > file-test.txt (Gera arquivo na pasta local)
10. $ aws s3 cp file-test-windows.txt s3://luizhsou1-storage (subir arquivo para S3)
11. $ aws s3 ls luizhsou1-storage (Lista o que tem dentro do bucket)

## Capítulo 2

### Conhecendo aplicações Serverlees

Aws foi pioneira na tecnologia de serverlees. 
Vantagens: Paga apenas pelo processamento que usar, evita despedircios, e o time de desenvolvimento não precisa se preocupar com nada de infra, elas se escalam sozinhas, fora que pode ser escrita em qualquer linguagem cada API.

**Programação orientada a eventos:**  Diversas formas de colher esses eventos, pode ser via http, cron jobs, rotina inteligente para algum tipo de log e receber esse evento e tomar essa decisão. Uma determinada ação, pode ser feita como uma pipeline, encadeando as funções para serem chamadas e executadas. Tem a fama de ser **Nano Serviços**

**Plataforma gerencia seu código**: O que torna difícil migração de serverlees, quando toma uma decisão de usar uma aplicação serverless, você meio que admite que tentará explorar o máximo o que essa cloud tem a te oferecer.

### Criar Lambda via interface gráfica

1. Acesse o serviço da AWS Lambda
2. Cria nova função
3. Selecione a trigger API Gateway, mas pode ter várias outras formas de gerar eventos para a lambda
4. REST API
5. Security Open (Pois queremos deixar essa de exemplo pública)
6. Gerará um link: https://pjycs9bl1f.execute-api.us-east-2.amazonaws.com/default/hello-interface?num1=10&num2=30

### Criar Lambda sem interface e sem framework (demo01)

Uma chatisse, precisa criar uma role, pegar o arn da role e vincular a function, rodar vários comandos.

### Qual tipo de tipo de aplicação vale a pena usar aws lambda ou aplicações serverless?

- As dependências são uma limitação (Onde as aplicações são executadas não temos controle, elas são executadas pela amazon em um CentOS)
- Nem sempre seu ambiente local é o que será executado na AWS Lambda, exemplo: Está rodando local o puppeteer no Windows, onde tem um exe do chrome, você cria o zip e sobe para amazon, provavelmente irá quebrar, pois a VM da amazon não entende a estrutura do binário do exe do windows.
- Se você não receber uma requisição por um determinado tempo, sua aplicação irá morrer dentro do ecossistema da AWS. Limpa o recurso e quando precisar de novo, ele levanta a máquina, e esse processo pode demorar um pouco (IDLE) (https://mikhail.io/serverless/coldstarts/aws/).
- **PRICING**: $0.20 por 1 milhão de requisição | O tempo é a chave do dinheiro, se você precisar gastar mais de um segundo, ou mais de 10 segundos, talvez as lambdas não são para seu problema.

- Link: https://cursosserverlessaws.club.hotmart.com/t/page/pRONDWXdeP (**MUITO IMPORTANTE ESSA AULA**)

## Capítulo 3



## Capítulo 4
## Capítulo 5
## Capítulo 6
## Capítulo 7
## Capítulo 8
## Capítulo 9
## Capítulo 10
## Capítulo 11
## Capítulo 12
## Capítulo 13 (Próximos passos)
