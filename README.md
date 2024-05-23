# mecajato
Cadastro de clientes e carros com serviços de mecânica e lavajato.


Comandos essenciais da Plataforma

create-states.py


        Adiciona os estados do Brasil não cadastrados nas tabelas dos clientes

        
# picc

## Documentação:

Acesse a documentação das APIs usando o Swagger ou ReDoc (/swagger ou /redoc):

- [Swagger](http://localhost:8000/swagger/)
- [ReDoc](http://localhost:8000/redoc/)


## Comandos essenciais da Plataforma:


### alter-user-password

        Help: Altera a senha de um usuário de todos os schemas
        Percorre todos os schemas onde é especificado um usuário para alteração da sua senha.
        É também retirado o status de superusuário, de membro da equipe e o status Ativo.

### create-states


        Adiciona os estados do Brasil não cadastrados nas tabelas dos clientes
        Se o registro de país "Brasil" não existir, é criado automaticamente nesse comando

