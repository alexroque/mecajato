# mecajato
Cadastro de clientes e carros com serviços de mecânica e lavajato.


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


### change-tipo-posse

        Help: Altera o tipo de posse das matrículas para "Arrendado sem especificação" as que tem a opção Área Arrendondada como sim.
        Percorre todos os schemas e verifica todas as matrículas que tem a opção área arredondada confirmada e altera a opção tipo
        posse para "Arrendado sem especificação"

### coliacao-crdc

        Help: Remove cadastros de CPRs na CRDC, pois, na CRDC, os cadastros são apagados diariamente


### compact-html

        Help: Compact html file losing extends django command



### create_default_colums

        Help: Inserindo configurações de colunas em tabela Instrumento de Crédito

        Percorre todos os schemas e configura as colunas da tabela do instrumento de crédito com as prioridades especificadas, os respectivos cabeçalhos padrões e na sequencia padrão já utilizado pelos clientes.

### create_user_in_schema

        Help: Cria um superusuário em um esquema específico

        Cria um superusuário com os dados do usuário(username, email, senha) e o schema especificados(schema_name) no comando.

### create-accounts-app

        Help: Command for create fast app



### create-configs-company-profile

        Help: Configura os campos que serão ocultados para cada empresa



### create-configs-unique-company

        Help: Configura os campos que serão ocultados para cada empresa



### create-docs

        Help: Cria novos tipos de CPR para migração lavoro



### create-fast-app

        Help: Command for create fast app



### create-monit-satelite-excel-v2

        Help: Cria monitoramentos satélites em instrumentos do Cluster Norte e Leste listados no arquivo excel



### create-monitoramento-satelite-excel

        Help: Cria monitoramentos satélites em instrumentos listados no arquivo excel



### create-operations

        Help: xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx



### create-people

        Help: 



### create-properties

        Help: 



### double

        Help: 



### fast-init

        Help: Starting project with fast



### generate-int-code

        Help: 



### migrate-docs-lavoro

        Help: 



### migrate-person-definition

        Help: 



### migrate-product-cpr

        Help: 



### minificate-css

        Help: Minificate css



### minificate-html

        Help: Minificate html



### minificate-js

        Help: Minificate javascript



### register-admin

        Help: Compact html file losing extends django command



### remove-crdc-registers

        Help: Remove cadastros de CPRs na CRDC, pois, na CRDC, os cadastros são apagados diariamente



### remove-repeated-people-lavoro

        Help: 



### remove-repeated-safra-lavoro

        Help: 



### update-notificados-monit-satelite

        Help: 
