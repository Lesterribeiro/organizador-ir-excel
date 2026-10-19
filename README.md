Sistema Unificado de Organização Fiscal – Imposto de Renda

Ferramenta analítica desenvolvida em Microsoft Excel para centralização, auditoria lógica e consolidação de dados fiscais e patrimoniais voltados à Declaração de Ajuste Anual do IRPF.
O projeto unifica todas as categorias obrigatórias da Receita Federal em uma única matriz de visualização integrada, aplicando rotinas lógicas que reduzem a incidência de erros de digitação e mitigam riscos de retenção em malha-fina.

Painel de Indicadores e Perguntas de Negócio

O topo da interface operacional disponibiliza cartões de controle macro que leem e consolidam em tempo real as movimentações das tabelas inferiores, respondendo a 3 perguntas essenciais de governança fiscal:
Volume Total de Rendimentos Ganhos:
	• Mapeamento: Calculado na célula B5. Realiza a soma integral dos rendimentos do trabalho (Tabela Tributáveis) com os lucros e dividendos isentos (Tabela Isentos).
Total de Despesas Dedutíveis Coletadas:
	• Mapeamento: Calculado na célula D5. Consolida todos os desembolsos passíveis de abatimento legal (Saúde e Educação) informados na planilha.
Evolução da Variação Patrimonial Líquida:
	• Mapeamento: Calculado na célula F5. Monitora o saldo líquido de evolução de bens móveis e imóveis, confrontando os anos-calendário anterior e atual.

Engenharia de Dados e Algoritmos de Cálculo

As seguintes diretrizes matemáticas foram implantadas nas linhas e colunas para automatizar a inteligência da planilha:

Consolidação com Filtro de Blocos (Células Indicadoras)

• Total de Rendimentos (B5): =SOMA(D9:D10)+SOMA(C14:C16)
• Total de Despesas (D5): =SOMA(D29:D30)
• Variação Patrimonial (F5): =SOMA(F20:F21)

Tratamento de Exceções e Auditoria de Campos

• Validação de Preenchimento (Status Campo - Coluna F9:F10):excel
=SE(OU(A9="";B9="";D9="");"⚠️ Campo Vazio";"OK")

Mecânica: Dispara um alerta textual imediato caso alguma linha de rendimento perca a integridade por falta de dados fundamentais (Fonte Pagadora, CNPJ ou Valor).
• Regra de Mutação de Ativos (Variação Patrimonial - Coluna F20:F21):excel
=SE(E20>=D20; E20-D20; 0)

Mecânica: Calcula o ganho de capital real ou desembolso financeiro incremental de bens e direitos, neutralizando variações contábeis negativas de depreciação linear.
• Filtro de Conformidade com o Teto Legal (Análise Limite - Coluna E29:E30):excel
=SE(E(A29="Educação";D29>3561,5); "⚠️ Ultrapassou Limite Individual"; "Elegível")

Mecânica: Analisa se as despesas de instrução inseridas ultrapassaram o teto dedutível individual anual permitido pela legislação vigente por CPF, alertando sobre a parcela não dedutível.


Dicionário Técnico de Estrutura de Linhas e Colunas

A planilha unificada organiza as informações sob os seguintes parâmetros relacionais:

Rendimentos Tributáveis (Linhas 8 a 11)

• Campos: Fonte Pagadora | CNPJ | Tipo de Rendimento | Valor Recebido | IRRF | Status Campo

Rendimentos Isentos e Não Tributáveis (Linhas 12 a 17)

• Campos: Tipo de Rendimento | Fonte Pagadora | Valor

Bens e Direitos (Linhas 18 a 22)

• Campos: Código RF | Descrição do Bem | Localização | Situação Ano Anterior | Situação Ano Atual | Variação Patrimonial

Dívidas e Ônus Reais (Linhas 23 a 26)

• Campos: Código RF | Credor / Instituição | Descrição da Dívida | Situação Ano Anterior | Situação Ano Atual

Despesas Dedutíveis (Linhas 27 a 31)

• Campos: Tipo de Despesa | Beneficiário | CPF / CNPJ | Valor | Análise Limite

Trilha de Comprovação Documental (Linhas 32 a 36)

• Campos: Categoria do Documento | Descrição do Arquivo | Status Comprovante | Link Digitalizador

Observação: Planilha desbloqueada para manipulação!
