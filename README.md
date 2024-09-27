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

 ### - Monitoramento dos pedidos em produção (SubMenu)
 ### Endpoint - /linha_producaos 
 ### List
    - Numero (Number: numero)
    - Cliente (String: pre_cadastro.nome_razao_social)
    - Vendedor (String: vendedor.parceiro.nome_razao_facial)
    - Modelo (String: modelo.descricao)
    - Qtd. (Number: qtd_original)
    - Criado dia (Date: data_hora)
    - Referência (String: referencia)
    - Entregar dia (Date: previsao_entrega)
    - Status do Pedido (String: status)
    - Status do Processo (Boolean: is_processo_finalizado)
    - Valor Total (Number: valor_total)
    - Status (String: status)

### Three 
    - pedidos
        - domaind_id
            - pre_cadastro
            - modelo
                - pecas
                - acabamentos
                - adicionais
                - materias
            - imagens
            - vendedor
                - parceiro
                    - enderecos
                    - contatos
            - itens
                - materia_prima
                - peca
                - etapa
                - adicionais
                - servicos
                - etapas
                - eventos

 ### - Pedidos Relacionados (SubMenu)
 ### Endpoint - /pedido_lotes 
 ### List
    - Numero Pedido (Number: numero_pedido)
    - Descrição de Linha de Produção (String: linha_producao_descricao)
    - Descrição do Modelo (String: modelo_descricao)
    - Vendedor (String: vendedor_nome)
    - Qtd. Itens Solicitados (Number: qtd_solicitada)
    - Qtd. Itens Produzidos (Number: qtd_produzida)
    - Valor Total (Number: valor_total)
    - Porcetagem de ganho bruto (Number: ganho_bruto)
    - Custo total do lote (Number: custo_total)
    - Data da solicitação (Date: data_solicitacao)
    - Status (String: status)

 ### - Gerenciamento dos pedidos em produção (SubMenu)
 ### Endpoint - /monitoramento 
 ### List
    - Numero (Number: numero)
    - Cliente (String: pre_cadastro.nome_razao_social)
    - Vendedor (String: vendedor.parceiro.nome_razao_facial)
    - Modelo (String: modelo.descricao)
    - Qtd. (Number: qtd_original)
    - Criado dia (Date: data_hora)
    - Referência (String: referencia)
    - Entregar dia (Date: previsao_entrega)
    - Status do Pedido (String: status)
    - Status do Processo (Boolean: is_processo_finalizado)
    - Valor Total (Number: valor_total)
    - Status (String: status)

 ### - Histórico do Pedido (SubMenu)
 ### Endpoint - /historico_detalhes 
 ### List
    - Criado em (Date: created_at)
    - Concluido em (String: ?)
    - Data de Solicitação (Date: data_hora)
    - Previsão de entrega (Date: previsao_entrega)
    - Pedidos Relacionados (Array: pedidos_relacionados)
    - Cliente (String: pre_cadastro_nome)
    - Vendedor (String: vendedor_nome)
    - Referência (String: referencia)
    - Modelo (String: modelo_descricao)
    - Linha de Montagem (String: linha_producao_descricao)
    - Localizador (String:  ?)
    - Quantidade Solicitada (Number: quantidade_solicitada)
    - Valor Unitário de Venda (Number: valor_unitario)
    - Valor Total de Vendas (Number: valor_total)
    - Quantidade de Erros nos Processos (Number: quantidade_erros_processo)
    - Quantidade produzida afetada por erros nos processos (Number: quantidade_afetada_erros_processo)
    - Quantidade Entregue no Pedido (Number: quantidade_entregue)
    - Quantidade Produzida (Number: quantidade_produzida)
    - Quantidade de Erros nas Peças (Number: quantidade_erros)
    - Valor Unitário de Custos por Errors nas Peças (Number: valor_unitario_custo_erro)
    - Valor Total de Custos por Erros nas Peças (Number: valor_total_custo_erro)
    - Valor de Custo Unitário de Fábricação (Number: valor_unitario_custo_fabricacao)
    - Valor Total de Custo de Fabricação (Number: valor_total_custo_fabricacao)
    - Resultado Final (Number: resultado)
    - Ficha técnica anexada pelo sistema (String: ficha_tecnica_nome)
    - imagens (Array: imagens)
