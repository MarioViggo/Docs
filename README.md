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

 ## - Orçamentos (Menu)
 ### - Gerar Orçamento (SubMenu)
 ### Endpoint - /orcamentos 
 ### List
    - Numero (Number: numero)
    - Cliente (String: pre_cadastro.nome_razao_social)
    - Vendedor (String: vendedor.parceiro.nome_razao_facial)
    - Criado em (Date: created_at)
    - Previsão da Entrega (Date: previsao_entrega)
    - Referência (String: referencia)
    - Modelo (String: modelo.descricao)
    - Tabela de Preço. (Object: tabela_preco_fabrica)
    - Valor Unitário (Number: precificacao.valor_unitario_vendedor)
    - Quantidade (Boolean: precificacao.quantidade)
    - Valor Total (Number: precificacao.valor_final)
    - Status (String: status)

 ### - Controle de Orçamentos (SubMenu)
 ### Endpoint - /orcamentos 
 ### List
    - Numero (Number: numero)
    - Cliente (String: pre_cadastro.nome_razao_social)
    - Vendedor (String: vendedor.parceiro.nome_razao_facial)
    - Criado em (Date: created_at)
    - Previsão da Entrega (Date: previsao_entrega)
    - Referência (String: referencia)
    - Modelo (String: modelo.descricao)
    - Tabela de Preço. (Object: tabela_preco_fabrica)
    - Valor Unitário (Number: precificacao.valor_unitario_vendedor)
    - Quantidade (Boolean: precificacao.quantidade)
    - Valor Total (Number: precificacao.valor_final)
    - Status (String: status)

 ## - Financeiro (Menu)
 ### - Movimentação Financeira (SubMenu)
 ### Endpoint - /movimentacao_financeiras 
 ### List
    - Conta/Parcela
    - Fornecedor (String: conta_pagar_parcelas.conta_pagar.fornecedor.parceiro.nome_razao_social)
    - Emitido Dia (Date: conta_pagar_parcelas.created_at)
    - Cobrança (Number: conta_pagar_parcelas.cobranca)
    - Vencimento (Date: conta_pagar_parcelas.vencimento)
    - VL Parcela (Number: conta_pagar_parcelas.conta_pagar.valor_total)
    - Dias (Number: ?)
    - Juros (Number: conta_pagar_parcelas.valor_juros)
    - VL desconto (Number: conta_pagar_parcelas.forma_pagto.nome)
    - Data pagamento (Date: conta_pagar_parcelas.pagamentos.data_hora)
    - VL Pago (Number: conta_pagar_parcelas.pagamentos.valor)
    - VL Pagar (Number: conta_pagar_parcelas.valor_total)
    - VL com juros (Number: totais.total_com_juros)
    - Status (String: conta_pagar_parcelas.status)
    - Qtd de parcelas (Number: totais.qtd_parcelas)
    - Total a pagar (Number: totais.total)
    - Total de juros (Number: totais.total_juros)
    - Total de desconto (Number: totais.total_desconto)
    - Total pago (Number: totais.total_pago)
    - Total (Number: totais.total)
 

## - Relatórios
### - Por entradas e saídas financeiras (SubMenu)
### Endpoint - /movimentacao_financeiras 
### List
    - Active (Boolean: active)
    - Conta Receber Pagamento ID (String: conta_receber_pagto_id)
    - Data MOvimento (Date: data_movimento)
    - Eventos (Array: eventos)
    - Eventos Status (String: eventos.status)
    - Eventos Status DH (Date: eventos.status_dh)
    - Eventos Status Por (Date: eventos.status_por)
    - Is Conciliado (Boolean: is_conciliado)
    - Nome Parceiro (String: nome_parceiro)
    - Numero (Number: numero)
    - Observação (String: observacao)
    - Portador Active: (Boolean: portador.active)
    - Portador Descricao: (String: portador.descricao)
    - Portador Descricao: (String: portador.descricao)
    - Portador Ligado a Terminal: (String: portador.ligado_a_terminal)
    - Portador Padrão: (Boolean: portador.padrao)
    - Portador Saldo: (Number: portador.saldo)
    - Portador Saldo Inicial: (Number: portador.saldo_inicial)
    - Portador Tipo: (String: portador.tipo)
    - Portador Ligado a Terminal: (String: portador.ligado_a_terminal)
    - Portador Ligado a Terminal: (String: portador.ligado_a_terminal)
    - Portador Ligado a Terminal: (String: portador.ligado_a_terminal)
    - Status (String: status)
    - Status DH (Date: status_dh)
    - Status Por (String: status_por)
    - q---Valor (Number: valor)

### Three 
    - movimenacao_financeiras
        - eventos
        - portador

## - Relatórios
### - Por Vendas (SubMenu)
### Endpoint - /vendas 
### List
    - Active: (Boolean: active)
    - Data: (Date: data_hora)
    - CPF/CNPJ: (String: cliente_cpf_cnpj)
    - Cliente: (String: cliente.parceiro.nome_razao_social)
    - Cliente Limite Crédito: (Number: cliente.limite_credito):
    - Vendedor: (Not on current response) 
    - Valor Bruto (R$): (Number: valor_bruto)
    - Total Desconto (R$): (Number: valor_desconto)
    - Total Acréscimo (R$): (Number: valor_desconto)
    - Valor Líquido (R$): (Number: valor_total)
    - Status: (String: cupom.status)

## - Relatórios
### - Relatórios por estoque de materiais (SubMenu)
### Endpoint - /categoria_materia_primas 
### List
    - Active: (Boolean: active)
    - Data: (Date: data_hora)
    - Classificação: (String: classificacao)
    - Código: (Number: codigo)
    - Descrição: (String: descricao):
    - Tag: (String: tag)

## - Relatórios
### - Relatórios por estoque de produtos (SubMenu)
### Endpoint - /categoria_produtos 
### List
    - Active: (Boolean: active)
    - Código: (Number: codigo)
    - Descrição: (String: descricao):

## - Configurações
### - Empresa (SubMenu)
### - Dados da empresa (SubMenu)
### Endpoint - /domains/{domaind_id}
### List
    - Active: (Boolean: active)
    - Name: (String: name)
    - Documento (String: doc)
    - Description: (String: description)
    - Display Name: (String: display_name)
    - Settings (JSON: settings)
    - Contacts Contact (String: contacts.contact)
    - Contacts Tag (String: contacts.tag)
    - Addresses Active: (Boolean: addresses.active)
    - Addresses Bairro: (String: addresses.bairro)
    - Addresses CEP: (String: addresses.cep)
    - Addresses Logradouro: (String: addresses.lougradouro)
    - Addresses Numero: (String: addresses.numero)
    - Addresses Ponto Referência: (String: addresses.ponto_referencia)
    - Addresses Municipio Active: (Boolean: addresses.municipio.active)
    - Addresses Municipio Código IBGE: (Number: addresses.municipio.codigo_ibge)
    - Addresses Municipio Nome: (String: addresses.municipio.nome)
    - Addresses Municipio RN: (String: addresses.municipio.silga_uf)

## - Configurações
### - Empresa (SubMenu)
### - Configuraçẽos da Empresa (SubMenu)
### Endpoint - /domains/{domaind_id}/settings
### PUT
    - Regras Caixa PDV Acréscimo Máximo: (Number: regras.caixa_pdv.acrescimo_max)
    - Regras Caixa PDV Bloquear Desconto: (Boolean: regras.caixa_pdv.bloquear_desconto)
    - Regras Caixa PDV Conferencia Auto: (Boolean: regras.caixa_pdv.conferencia_auto)
    - Regras Caixa PDV Desconto Máximo: (Number: regras.caixa_pdv.desconto_max)
    - Regras Caixa PDV Fechamento as cegas: (Boolean: regras.caixa_pdv.fechamentos_as_cegas)
    - Regras Caixa PDV Forçar Fechamento Caixa: (Boolean: regras.caixa_pdv.forcar_fechamento_caixa)
    - Regras Caixa PDV Registro Caixa: (Boolean: regras.caixa_pdv.registro_caixa)
    - Regras Config Financeira Operação Padrão Pagar: (String: regras.config_financeira.operacao_padrao_pagar)
    - Regras Config Financeira Operação Padrão Receber Caixa: (String: regras.config_financeira.operacao_padrao_receber_caixa)
    - Regras Config Financeira Operação Padrão Receber Fábrica: (String: regras.config_financeira.operacao_padrao_receber_fabrica)
    - Regras Config Financeira Operacoes Operacao: (String: regras.config_financeira.operacoes.operacao)
    - Regras Controle Cliente Limite Crédito: (Boolean: regras.controle.cliente.limite_credito)
    - Regras Controle Cliente Saldo Crédito: (Boolean: regras.controle.cliente.saldo_credito)
    - Regras Controle Contas Receber Contas Atraso: (String: regras.controle.conta_receber.contas_atraso)
    - Regras Controle Contas Receber Dias Tolerancia Juros: (Number: regras.controle.conta_receber.dias_tolerancia_juros: 2)
    - Regras Controle Contas Receber Taxa Juros Mẽs: (Number: regras.controle.conta_receber.taxa_juro_mes)
    - 