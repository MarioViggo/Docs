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
 ### - Categoria de Matérias Primas (SubMenu)
 ### Endpoint - /categoria_materia_primas 
 ### List
    - Código (Number: codigo)
    - Descrição (String: descricao)
    - Classficação (String: classficacao)
    - tag (String: tag)

### - Matéria Prima (SubMenu)
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


### - Entrada (SubMenu)
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

### - Saída (SubMenu)
### Endpoint - /rses 
    - Numero (Number: numero)
    - Data (Date: data)
    - Observação (Date: observacao)
    - Status (String: status)

### Three 
    - rees
        - domaind_id
            - itens
    
### - Transformação de matéria (SubMenu)
### Endpoint - /tmps 
    - Numero (Number: numero)
    - Data (Date: data_hora)
    - Observação (String: observacao)
    - Status (String: status)

### Three 
    - rees
        - domaind_id
            - itens
            - servicos

### - Ajuste de estoque (SubMenu)
### Endpoint - /ajuste_materias 
    - Numero (Number: numero)
    - Data (Date: data_hora)
    - Observação (Date: observacao)
    - Status (String: status)

### Three 
    - rees
        - domaind_id
            - itens
    
### - Variações matéria prima (SubMenu)
### Endpoint - /variacao_materias 
    - Descrição (String: descricao)

 ## - Produto Acabado (Menu)
 ### - Categorias do produto (SubMenu)
 ### Endpoint - /categoria_produtos 
 ### List
    - Código (Number: codigo)
    - Descrição (String: descricao)

 ### - Tabela de preços (SubMenu)
 ### Endpoint - /tabela_precos 
 ### List
    - Código (Number: codigo)
    - Nome (String: nome)

 ### - Produtos (SubMenu)
 ### Endpoint - /produtos 
 ### List
    - Código (Number: codigo)
    - Código de Barras (String: nome)
    - Código de Barras (String: nome)
    - Descrição (String: descricao)
    - Estoque (String: quantidade)
    - Estoque Mínimo (String: qtd_variacoes)
    - Valor Unitário (String: valor_unitario)
    - Em Grade (String: usa_grade)

### Three 
    - produtos
        - domaind_id
            - categoria
            - unidade
            - imagens
            - preços
            - fornecedores
    
 ### - Entrada (SubMenu)
 ### Endpoint - /ree_produtos 
 ### List
    - Numero (Number: numero)
    - Data (Date: data)
    - Fornecedor (String: forncededor.nome_razao_social)
    - Status (String: status)

### Three 
    - ree_produtos
        - domaind_id
            - fornecedor
                - enderecos
                - contatos
            - produtos

 ### - Saida (SubMenu)
 ### Endpoint - /rse_produtos 
 ### List
    - Numero (Number: numero)
    - Data (Date: data)
    - Observação (String: observacao)
    - Status (String: status)

### Three 
    - ree_produtos
        - domaind_id
            - produtos

 ### - Entrada de produtos via pedido (SubMenu)
 ### Endpoint - /tpe_produtos 
 ### List
    - Numero (Number: numero)
    - Data (Date: data)
    - Observação (String: observacao)
    - Status (String: status)

### Three 
    - ree_produtos
        - domaind_id
            - itens

 ### - Variações de produto (SubMenu)
 ### Endpoint - /variacoes 
 ### List
    - Descrição (String: descricao)

 ### - Grade de Produtos (SubMenu)
 ### Endpoint - /produto_variacoes 
 ### List
    - SKU (String: sku)
    - Código de Barras (Date: data)
    - Categoria (String: produto.categoria.descricao)
    - Descrição (String: descricao)
    - Estoque (String: quantidade)
    - Estoque Mínimo (String: qtd_minima)
    - Valor (String: valor)

### Three 
    - ree_produtos
        - domaind_id
            - produto
                - settings_variacoes
                - categoria
                - precos
                - fornecedores
            - identificadores