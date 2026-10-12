⚓ Desafio LH Nautical — Engenharia de Dados e IA

Este repositório contém a resolução completa do desafio técnico de dados para o varejo "LH Nautical", englobando todo o ciclo de engenharia de dados, análise e aprendizado de máquina. O projeto foi desenvolvido em Python e SQL (PostgreSQL).

🛠️ Tecnologias Utilizadas

Python 3: Lógica principal, inferência de schemas e modelagem.

Bibliotecas Python: pandas, psycopg2, scikit-learn, numpy.

Banco de Dados: PostgreSQL (criação automática de schema e ingestão via COPY).

Visualização: Dashboard interativo em HTML/CSS.

📊 Estrutura das Análises (7 Singraduras)

O desafio foi dividido em sete etapas cruciais, documentadas no notebook principal:

Exploração de Dados: Diagnóstico da tabela bruta de pedidos (48.998 registros), identificação de outliers (via IQR) e filtragem de status inconsistentes (rascunhos/cancelados).

Geração Automática de Schema: Script em Python que lê 24 arquivos CSV e infere dinamicamente a tipagem dos dados para criar o arquivo schema.sql.

Carga de Dados no Banco: Pipeline de ingestão otimizado utilizando o comando COPY do PostgreSQL, carregando mais de 250 mil linhas.

Mapeamento de Clientes Fiéis: Consultas SQL complexas com cruzamento de 4 tabelas para identificar os top 10 clientes com maior ticket médio e alta diversidade de compra (mais de 13 categorias).

Dimensão de Calendário: Criação de uma tabela de dimensão temporal em SQL para corrigir vieses de dias sem vendas em lojas físicas, revelando o real desempenho diário.

Previsão de Demanda: Implementação de um modelo baseline de média móvel de 3 meses para a "Bússola de Bordo 702", com validação e cálculo da métrica MAE.

Sistema de Recomendação: Motor de recomendação baseado em Similaridade de Cosseno (Scikit-Learn) focado no comportamento de compra dos usuários (matriz de interação Usuário x Produto).

📁 Arquivos do Repositório

analise_lh_nautical.ipynb: Jupyter Notebook com o código Python, consultas SQL e explicações detalhadas de cada etapa.

Dashboard_LH_Nautical.html / .pdf: Diário de bordo e relatório visual sumarizando os principais achados e KPIs do projeto.

schema.sql: (Opcional) Arquivo gerado dinamicamente para criação das tabelas no banco de dados.

🚀 Como Executar

Clone o repositório:

git clone https://github.com/Bonnier98/desafio-lh-nautical.git


Instale as dependências:

pip install pandas psycopg2-binary scikit-learn numpy


Configure a string de conexão do PostgreSQL no seu ambiente (ex: Neon DB).

Execute o Jupyter Notebook analise_lh_nautical.ipynb.

Projeto desenvolvido como resolução do desafio técnico de Dados.
