## Configurações e teste inicial com S3

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

## Capítulo 1
## Capítulo 2
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
