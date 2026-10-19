Guia de Operação e Uso da Ferramenta Fiscal

Este guia orienta o usuário final no preenchimento seguro e correto da planilha unificada para evitar erros lógicos de digitação. 

Sequência Correta de Preenchimento

Para garantir a integridade dos cálculos do painel superior, execute o preenchimento de baixo para cima nas tabelas operacionais: 

**Passo 1: Entradas de Renda** 

  * Preencha as linhas 9 e 10 do bloco de Rendimentos Tributáveis.
  * Insira os proventos isentos (como dividendos de FIIs ou lucros de PJ) nas linhas 14 a 16.
**Passo 2: Declaração Patrimonial** 

  * Atualize os saldos das contas e valores de compra de bens nas linhas 20 e 21. O sistema calculará a variação patrimonial automaticamente.
**Passo 3: Mapeamento de Obrigações** 

  * Insira o saldo devedor de empréstimos nas linhas 24 e 25.
**Passo 4: Deduções da Base** 

  * Lance os gastos com planos de saúde e mensalidades escolares nas linhas 29 e 30.

### ⚠️ Interpretando as Sinalizações de Alerta

O sistema possui gatilhos de segurança visuais em texto para avisar sobre dados inconsistentes: 

* **Alerta "⚠️ Campo Vazio" (Coluna F):** Indica que a linha foi iniciada mas falta preencher informações cruciais (CNPJ ou Valor). Complete o campo para reativar o cálculo daquela linha.
* **Alerta "⚠️ Ultrapassou Limite Individual" (Coluna E):** Disparado quando o gasto em educação ultrapassa o limite individual dedutível determinado pela Receita Federal. O alerta avisa que a diferença não reduzirá o imposto na declaração oficial.
* **Resultado #REF! nos Indicadores:** Ocorre se linhas intermediárias das tabelas forem deletadas incorretamente, quebrando a matriz de soma. Utilize o comando Ctrl + Z para restaurar e limpe os dados apenas selecionando as células e apertando a tecla Delete.
