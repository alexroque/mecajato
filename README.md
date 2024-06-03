# mecajato
Cadastro de clientes e carros com serviços de mecânica e lavajato.

# picc

## Documentação:

Acesse a documentação das APIs usando o Swagger ou ReDoc (/swagger ou /redoc):

- [Swagger](http://localhost:8000/swagger/)
- [ReDoc](http://localhost:8000/redoc/)


## Comandos essenciais da Plataforma:


### python manage.py alter-user-password

        Help: Altera a senha de um usuário de todos os schemas.
        
        É especificado um usuário, onde se percorre todos os schemas onde é alterado sua senha.
        É também retirado o status de superusuário, de membro da equipe e o status Ativo.

### python manage.py change-tipo-posse

        Help: Altera o tipo de posse das matrículas para "Arrendado sem especificação" as que tem a opção Área 
        Arrendondada como sim.

        Percorre todos os schemas e verifica todas as matrículas que tem a opção área arredondada confirmada e altera 
        a opção tipo posse para "Arrendado sem especificação"

### python manage.py coliacao-crdc

        Help: Cria um registro no model CRDCInstrumentRequest, obtendo as conciliações exceto do mês corrente.

        Filtra o model CRDCInstrument obtendo os registros com o campo was_conciliated igual a False, ou seja, os não 
        conciliados, exceto os registros do mês corrente, verifica os hashs válidos e faz a conciliação com a rota 
        dada e os dados da api. Por fim, cria um registro no model CRDCInstrumentRequest com os valores obtidos.

### python manage.py compact-html

        Help: Compact html file losing extends django command

        Compacta o arquivo html dado utilizando uma api que remove espaços em branco,  linhas em branco, comentários 
        html, css, javascript e comentários django.

### python manage.py create_default_colums

        Help: Inserindo configurações de colunas em tabela Instrumento de Crédito

        Percorre todos os schemas e configura as colunas da tabela do instrumento de crédito com as prioridades 
        especificadas, os respectivos cabeçalhos padrões e na sequencia padrão já utilizado pelos clientes.

### python manage.py create_user_in_schema

        Help: Cria um superusuário em um esquema específico

        Cria um superusuário com os dados do usuário(username, email, senha) e o schema especificados(schema_name) no 
        comando.

### python manage.py create-accounts-app

        Help: Command for create fast app

        Cria um novo app chamado "accounts" onde há uma pasta chamada "app" que possibilita a criação de vários apps 
        centralizados em um mesmo local. Pode ser utilizado quando há vários apps com objetivos semelhantes.

### python manage.py create-configs-company-profile

        Help: Configura os campos que serão ocultados para cada empresa

        Configura os campos do instrumento de crédito a serem ocultados para cada schema. Configura também as abas 
        que serão ocultadas na tela do instrumento de crédito. 

### python manage.py create-configs-unique-company

        Help: Configura os campos que serão ocultados para cada empresa

        Adiciona os campos únicos de cada schema aos outros schemas para serem ocultados. Os campos únicos de cada 
        schema não são permitidos em schema diferente.

### python manage.py create-docs

        Help: Cria novos tipos de CPR para migração lavoro

        Cria novos modelos de documento para a migração da lavoro. Somente o título é criado, sem que se crie o nome 
        do arquivo.  


### python manage.py create-fast-app

        Help: Command for create fast app

        Cria um novo app onde há uma pasta chamada "app" que possibilita a criação de vários apps centralizados em um 
        mesmo local. Pode ser utilizado quando há vários apps com objetivos semelhantes. 


### python manage.py create-monit-satelite-excel-v2

        Help: Cria monitoramentos satélites em instrumentos do Cluster Norte e Leste listados no arquivo excel

        Cria monitoramentos satélites para os clusters norte e leste com os respectivos notificados em 
        cada cluster a partir de um arquivo excel.

### python manage.py create-monitoramento-satelite-excel

        Help: Cria monitoramentos satélites em instrumentos listados no arquivo excel

        Cria monitoramentos satélites para os clusters norte, leste e sul com os respectivos notificados em 
        cada cluster a partir de um arquivo excel.

### python manage.py create-operations

        Help: Cria instrumentos de crédito a partir do arquivo dado.

        Com base no arquivo dado, é criado instâncias de instrumento de crédito com os dados contidos no arquivo, 
        como safras, propriedades, matrículas entre outros dados.

### python manage.py create-people

        Help: Cria as pessoas dadas no arquivo

        Cria as pessoas que estão no arquivo adaptando os campos existentes da LAVORO para os campos existentes 
        na PICC. Se alguma pessoa já for cadastrada na PICC com o documento, este registro não é criado novamente.

### python manage.py create-properties

        Help: Cria as propriedades com as informações dadas no arquivo especificado.

        Verifica a existência dos dados no arquivo se constam na banco de dados da plataforma, senão existirem são 
        criados seguindo a sequencia lógica de criação dos dados. Por fim, são criados as propriedades.

### python manage.py create-states

        Help: Adiciona os estados do Brasil não cadastrados nas tabelas dos clientes.
        
        Pode se escolher em percorrer todos os schemas ou um schema específico. É adicionado todos os estados do 
        Brasil, ou os que estão em falta na tabela de UF.  
        Se o registro de país "Brasil" não existir, é criado automaticamente nesse mesmo comando antes da criação dos
        estados.

### python manage.py generate-int-code

        Help: Gera um código inteiro para o campo integer_code do model Client.

        Percorre todos os registros do model Client, verifica se o campo integer_code está preenchido, 
        se não estiver, gera um código aleatório de 8 dígitos e salva. 

### python manage.py migrate-docs-lavoro

        Help: Faz a migração dos arquivos da LAVORO para a PICC.

        Percorre todos os intrumentos migrados da LAVORO, obtém os ids e faz o download de todos os 
        documentos na plataforma que eles usavam. Com os arquivos obtidos, são salvos na plataforma
        PICC em seus respectivos instrumentos.

### python manage.py migrate-person-definition

        Help: Corrige as definições do model Person.

        Percorre os registros do model Person e verifica se os registros estão corretos conforme a sua 
        definição e onde está sendo utilizado. Corrige as definições de Unidade Loja, Investida e Credora para seus 
        devidos fins e o restante dos campos(ex: proprietário, emitente, avalista e os demais) são modificados para 
        a definição de Cliente.

### python manage.py migrate-product-cpr

        Help: Popula o model DadosParcelamento e FormaPagamentoCPRFisica com os dados dos campos existentes no 
        InstrumentoCredito.

        Percorre o model InstrumentoCredito obtendo os dados de quantidade de parcelas e a forma de pagamento e 
        popula os models FormaPagamentoCPRFisica e DadosParcelamento com os respectivos dados.


### python manage.py minificate-css

        Help: Minificate css

        Minifica o arquivo css fornecido como parâmetro

### python manage.py minificate-html

        Help: Minificate html

        Minifica o arquivo html fornecido como parâmetro

### python manage.py minificate-js

        Help: Minificate javascript

        Minifica o arquivo javascript fornecido como parâmetro

### python manage.py register-admin

        Help: Registra o model no admin 

        Registra o model no admin do app passado como parâmetro. É necessário passar o app com o model
        (ex: aml.recebivel).

### python manage.py remove-crdc-registers

        Help: Remove cadastros de CPRs na CRDC, pois, na CRDC, os cadastros são apagados diariamente

        Seleciona todos os registros do model CRDCInstrument que possui instrumento de crédito vinculado, 
        deleta todos esses registros, a seguir seleciona todos os registros do model CRDCInstrumentRequest
        e também deleta todos os registros. Por fim, faz o update do model InstrumentoCredito setando toda 
        a tabela com o campo was_registered_at_CRDC como False. 

### python manage.py remove-repeated-people-lavoro

        Help: Remove registros no model Person onde se tem os dados duplicados no campo document

        Verifica no schema dado se existe documentos duplicados na tabela Person. Percorre o model Person 
        e verifica com base numa lista dada de documentos se existem registros com documentos duplicados.
        Se existirem documentos duplicados, deleta todos os registros duplicados, com exceção do que tem o
        campo definicao como UNIDADE LOJA e o primeiro deles que foi criado.

### python manage.py remove-repeated-safra-lavoro

        Help: Remove registros no model Safra onde os dados do campo Ano está duplicado.

        Verifica os registros do model Safra se existe registros duplicados com base no campo ano, deletando 
        os duplicados e mantendo o que foi criado primeiro.

### python manage.py update-notificados-monit-satelite

        Help: Atualiza o MonitoramentoSateliteV2Instrumento no campo notificados com uma lista de usuários. 
        
        Percorre o model MonitoramentoSateliteV2Instrumento limpando o campo notificados e inserindo os 
        valores da lista dada no comando. Esta ação é executada somente no cluster também dado no comando.
        Faz o update para todos os registros do model MonitoramentoSateliteV2Instrumento que contém o cluster dado.
