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

        Help: Altera a senha de um usuário de todos os schemas.
        É especificado um usuário, onde se percorre todos os schemas onde é alterado sua senha.
        É também retirado o status de superusuário, de membro da equipe e o status Ativo.

### create-states

        Help: Adiciona os estados do Brasil não cadastrados nas tabelas dos clientes.
        Pode se escolher em percorrer todos os schemas ou um schema específico. É adicionado todos os estados do Brasil,
        ou os que estão em falta na tabela de UF.  
        Se o registro de país "Brasil" não existir, é criado automaticamente nesse mesmo comando antes da criação dos estados.

