# Entities 

## - Cliente
### Endpoint - /pre_cadastros
### List
    - Código (Number: codigo)
    - Apelido/Nome Fantasia
    - Nome/Razão Social (String: nome_razao_social)
    - CPF/CNPJ (Number: cliente.pareceiro.cpf_cnpj)
    - Limite Crédito (Number: cliente.limite_credito)
    - Saldo Limite Crédito (Number: cliente.saldo_limite_credito)
    - Saldo de Crédito (Number: cliente.saldo_credito)
    - Active (Boolean: active)
    - Domain ID (String: cliente.domaind_id)

### Three 
    - pre_cadastros
        - domaind_id
        - cliente
            - parceiro
                - enderecos
                - contatos

## - Fornecedores
### Endpoint - /forncededores 
### List
    - Código (Number: codigo)
    - Nome/Razão Social (String: parceiro.nome_razao_social)
    - Nome Fantasia (String: parceiro.apelido_nome_fantasia)
    - CPF/CNPJ (Number: parceiro.pareceiro.cpf_cnpj)
    - Active (Boolean: active)

### Three 
    - fornecedores
        - domaind_id
            - parceiro
                - enderecos
                - contatos

## - Fabricantes
### Endpoint - /fabricantes 
### List
    - Código (Number: codigo)
    - Nome/Razão Social (String: parceiro.nome_razao_social)
    - CPF/CNPJ (Number: parceiro.pareceiro.cpf_cnpj)
    - Insc. Estadual/RG (String: parceiro.rg_insc_est)

### Three 
    - fabricantes
        - domaind_id
            - parceiro
                - enderecos
                - contatos

## - Funcionario
### Endpoint - /funcionarios 
### List
    - Código (Number: codigo)
    - Nome/Razão Social (String: parceiro.nome_razao_social)
    - Nome Fantasia (String: parceiro.apelido_nome_fantasia)
    - CPF/CNPJ (Number: parceiro.pareceiro.cpf_cnpj)
    - Usuário (String: parceiro.user.name)

### Three 
    - fornecedores
        - domaind_id
            - parceiro
                - enderecos
                - contatos
                - user
                - etapas
                - processos

## - Vendedor
### Endpoint - /vendedores 
### List
    - Código (Number: codigo)
    - Nome/Razão Social (String: parceiro.nome_razao_social)
    - Nome Fantasia (String: parceiro.apelido_nome_fantasia)
    - CPF/CNPJ (Number: parceiro.pareceiro.cpf_cnpj)
    - Insc. Estadual/RG (String: parceiro.rg_insc_est)
    - Usuário (String: parceiro.user.name)
    - Tipo (String: tipo)
    - Saldo de Crédito (Number: parceiro.saldo_credito)

### Three 
    - fornecedores
        - domaind_id
            - carteira
            - parceiro
                - enderecos
                - contatos
 
 ## - Matéria Prima (Menu)
 ## - Categoria de Matérias Primas (SubMenu)
 ### Endpoint - /categoria_materia_primas 
 ### List
    - Código (Number: codigo)
    - Descrição (String: descricao)
    - Classficação (String: classficacao)
    - tag (String: tag)

## - Matéria Prima (Menu)
## - Matéria Prima (SubMenu)
### Endpoint - /materia_primas 
### List
    - Código (Number: codigo)
    - Descrição (String: descricao)
    - Unidade (String: categoria.unidade.descricao)
    - Categoria de Matéria Prima (String: categoria.descricao)
    - Estoque (Number: quantidade)
    - Estoque Mínimo (Number: qnd_minima)
    - Valor  (Number: valor)
    - Em Grade (String: usa_grade)

### Three 
    - materia_primas
        - domaind_id
            - categoria
            - unidade
            - fornecedores

## - Matéria Prima (Menu)
## - Entrada (SubMenu)
### Endpoint - /rees 
    - Numero (Number: numero)
    - Data (Date: data)
    - Data de Compra (Date: data_compra)
    - Data de Recebimento (Date: data_recebimento)
    - Fornecedor (String: forncedor.nome_razao_social)
    - Status (String: status)

### Three 
    - rees
        - domaind_id
            - fornecedor
                - enderecos
                - contatos
            - itens