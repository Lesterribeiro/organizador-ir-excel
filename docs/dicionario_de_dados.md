Dicionário de Dados – Sistema de Organização Fiscal

Este documento descreve a estrutura técnica, os tipos de dados e as regras de consistência lógica aplicadas às colunas da planilha unificada. 

Bloco: Rendimentos Tributáveis

ColunaNome TécnicoTipo de DadoValidação / Regra de Negócio
****A****
Fonte PagadoraAlfanumérico (Texto)Preenchimento obrigatório da razão social ou nome.
****B****
CNPJTexto MascaradoDeve conter 14 dígitos numéricos formatados: 00.000.000/0000-00.
****C****
Tipo de RendimentoAlfanumérico (Texto)Classificação do provento (Ex: Salário, Pró-labore, Aluguel).
****D****
Valor RecebidoNumérico (Moeda R$)Valor bruto acumulado. Deve ser maior ou igual a zero.
****E****
IRRFNumérico (Moeda R$)Imposto de Renda Retido na Fonte. Não pode ser maior que o Valor Recebido.
****F****
Status CampoFórmula LógicaValida se há campos em branco e emite alerta de consistência.

Bloco: Bens e Direitos

ColunaNome TécnicoTipo de DadoValidação / Regra de Negócio
****A****
Código RFAlfanumérico (Texto)Código oficial da Receita Federal (Ex: 11 - Apartamento).
****B****
Descrição do BemAlfanumérico (Texto)Detalhamento, endereço, placa ou características de aquisição.
****C****
LocalizaçãoAlfanumérico (Texto)País de origem do bem/direito.
****D****
Situação Ano AnteriorNumérico (Moeda R$)Saldo financeiro do ativo em 31/12 do ano-calendário anterior.
****E****
Situação Ano AtualNumérico (Moeda R$)Saldo financeiro do ativo em 31/12 do ano-calendário atual.
****F****
Variação PatrimonialFórmula LógicaCalcula o acréscimo patrimonial (Ano Atual - Ano Anterior).

Bloco: Despesas Dedutíveis

ColunaNome TécnicoTipo de DadoValidação / Regra de Negócio
****A****
Tipo de DespesaAlfanumérico (Texto)Classificação legal do gasto (Ex: Saúde, Educação).
****B****
BeneficiárioAlfanumérico (Texto)Nome do profissional, clínica ou instituição de ensino.
****C****
CPF / CNPJTexto MascaradoCadastro oficial do prestador de serviço para cruzamento de dados.
****D****
ValorNumérico (Moeda R$)Gasto total efetuado comprovado por nota fiscal ou recibo.
****E****
Análise LimiteFórmula LógicaVerifica se a despesa de instrução estourou o teto individual anual.
