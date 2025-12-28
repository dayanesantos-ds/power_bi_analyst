## 📊 Criando um Dashboard corporativo com integração com SQL Server e Azure - Desafio DIO

### 📊 Acesse o Relatório

👉 *Visualizar no Power BI Service:*  
https://app.powerbi.com/view?r=eyJrIjoiNWM5MDBlNTMtN2YwYS00MmUyLTk0Y2MtYTBiZDdkYTY1NzBjIiwidCI6IjQ5ZjM1ZjU0LTIyMjAtNDVmMS1iZmFlLTgzOWEyZGE1NjhkNCJ9

### 🧾 Visão Geral

Este projeto integração e análise de dados corporativos utilizando:

🖥️ SQL Server hospedado na Azure

⚙️ Power Query para limpeza e transformação dos dados

📊 Power BI para criação de Relatórios analíticos 

O objetivo foi transformar a base fornecida no desafio da DIO, para gerar insights sobre funcionários, gerentes, departamentos e projetos.

### 🛠️ 1. Criação do Banco no Azure SQL Server

Etapas foram realizadas:

✔ Criação de uma instância SQL Server na Azure

✔ Configuração de firewall e permissões de acesso

✔ Ajuste do script do desafio para dialeto T-SQL

✔ Criação das tabelas no banco

✔ Validação no SQL Server Management Studio

✔ Conexão do banco ao Power BI Desktop

O script original exigiu ajustes porque não estava 100% compatível com SQL Server.

### 🧹 2. Limpeza e Transformação de Dados (Power Query)

Principais etapas executadas:

Padronização de colunas e formatos

Correção de tipos de dados (ex.: salário → decimal)

Tratamento de nulos e inconsistências

Remoção de colunas redundantes

Criação de colunas derivadas

Alteração de nome das culunas

Mescla de tabelas para enriquecer informações

🔎 Verificações de Qualidade Aplicadas

Funcionários sem gerente cadastrado 

Departamentos sem gerente associado

Projetos sem registro de horas

Funcionários com múltiplos projetos

Busca e eliminação de duplicidades

### 🔗 3. Modelagem do Banco para Análise

📌 Mesclas e Tabelas Enriquecidas

Employee + Department

Employee + Dependentes

Employee + Gerentes

Employee + work hours

Inclui:

Funcionário

Departamento

Local do Departamento

Relação Gerente x Funcionários

Relacionamento via ID gerente

Casos sem gerente → categorizados como "No Gerent"

James aparece sem gerente no dataset e mantivem o registro conforme a fonte, documentando o caso.
No conjunto de dados, James não possuía horas registradas. Para consistência analítica, adotei 40h padrão, com registro explícito na documentação.

### 🧮 4. Métricas Criadas (DAX)

Hours by departament

Hours by Gerent


Hours by location

Employees by location



🎯 Modelagem

Relacionamento principal: Employee-ID

Correção de cardinalidade

Estrutura próxima ao modelo estrela

### 📊 5. Dashboards Criados

 🟣 Página 1 — Análise Geral de Funcionários

Inclui:

Total Salary

Total Horas trabalhadas

Horas trabalhadas por Funcionário

Horas trabalhadas por Gerente

Quantidade Funcionários por Gerente

Salário por Local do Departamento

Quantidade de Funcionários por Local

👉 Foco: visão executiva / indicadores principais

🔵 Página 2 — Análise por Local, Projeto e Gerente

Inclui:

Total Horas por Local do Projeto

Horas por Departamento + Local

Total Horas por Projeto

Tabela analítica detalhada funcionários e horas

👉 Foco: exploração operacional e detalhamento

### 🧠 6. Decisões Analíticas Importantes

Nenhum valor foi inventado sem justificativa

Casos especiais foram documentados

Relações ambíguas tratadas com USERELATIONSHIP quando necessário

Priorização de clareza analítica vs. excesso de gráficos

Design orientado a storytelling de dados

### 🚀 7. Resultados Obtidos

Base bruta transformada em informação confiável

Modelo analítico consistente

Dashboards claros e interativos

Insights sobre:

carga de trabalho

hierarquia organizacional

distribuição de horas


### ✨ Possíveis Evoluções

Refatoração para modelo estrela completo (DimTables)

Séries temporais (horas por período)

Métricas financeiras por projeto

Publicação no Power BI Service

### 🏁 Conclusão

Este projeto completa o ciclo de Business Intelligence:

Azure SQL ➝ Power Query ➝ Modelagem ➝ DAX ➝ Dashboards ➝ Insights

Ele demonstra a importância de:

validar dados,modelar corretamente,documentar decisões,
pensar como analista — e não apenas operador de ferramenta.

### 📚 Tecnologias Utilizadas

SQL Server Azure

Power BI Desktop

Power Query

DAX

SQL Server Management Studio

🙋 Sobre o Projeto

Este projeto foi desenvolvido como parte de um desafio técnico de análise de dados e BI.

### 🖼️ Visualizações do Dashboard

![Página 1](https://github.com/dayanesantos-ds/power_bi_analyst/blob/main/desafio-power-bi/imagens/pag%201%20relatorio.png)
![Página 2](https://github.com/dayanesantos-ds/power_bi_analyst/blob/main/desafio-power-bi/imagens/pag%202%20relatorio.png)
![Página 3](https://github.com/dayanesantos-ds/power_bi_analyst/blob/main/desafio-power-bi/imagens/sql%20azure%201.png)
![Página 4](https://github.com/dayanesantos-ds/power_bi_analyst/blob/main/desafio-power-bi/imagens/sql%20azure%202.png)



