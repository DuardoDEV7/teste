Dashboard de Saúde Digital: Sono, Estresse e Uso de Celular
Este projeto realiza o ciclo completo de análise de dados (ETL) e visualização de informações sobre o impacto do uso de dispositivos móveis na qualidade do sono e nos níveis de estresse de 15.000 usuários.

Sobre o Projeto:
O objetivo principal é entender como variáveis como tempo de tela, consumo de cafeína e ocupação influenciam o bem-estar mental e a qualidade do descanso. O projeto está dividido em duas partes:

Pipeline de ETL: Limpeza, tratamento e transformação dos dados brutos.

Dashboard Interativo: Visualização de indicadores-chave de desempenho (KPIs) utilizando Streamlit.

Estrutura do Repositório
data/sleep_mobile_stress_dataset_15000.csv: Base de dados original (Kaggle).

limpeza_dados.py: Script responsável pela limpeza e preparação dos dados.

dashboard.py: Aplicação Streamlit para visualização interativa.

data/sleep_clean.csv: Arquivo gerado após o processamento, pronto para consumo.

Tecnologias Utilizadas
Linguagem: Python 3

Manipulação de Dados: Pandas

Visualização de Dados: Matplotlib, Seaborn

Interface Web: Streamlit

Processo de ETL (Extract, Transform, Load)
O script de transformação realiza as seguintes etapas:

Extração: Leitura do arquivo CSV original.

Limpeza: Remoção de duplicatas e tratamento de valores ausentes (preenchimento com 0 ou média).

Transformação: * Criação da coluna categoria_estresse (Baixo, Médio, Alto) via binning.

Cálculo de métricas agrupadas por profissão.

Carga: Exportação do DataFrame limpo para um novo arquivo CSV otimizado para o dashboard.

Como Executar
1. Instalação das Dependências
Certifique-se de ter as bibliotecas necessárias instaladas:

Bash
pip install pandas streamlit seaborn matplotlib
2. Executar a Limpeza de Dados (ETL)
Primeiro, processe os dados brutos:

Bash
python limpeza_dados.py
3. Iniciar o Dashboard
Após gerar o arquivo sleep_clean.csv, inicie a interface:

Bash
streamlit run dashboard.py
Funcionalidades do Dashboard
Filtro por Ocupação: Analise dados específicos de Designers, Engenheiros de Software, Professores, etc.

Análise de Estresse: Gráfico de pizza mostrando a distribuição dos níveis de estresse.

Qualidade do Sono: Indicador circular (rosca) segmentando a qualidade entre Baixa, Regular e Alta.

Hábitos de Risco: Monitoramento de uso excessivo de celular (>6h) e consumo elevado de cafeína.

Matriz de Correlação: (Disponível no script de análise) Identifica a relação matemática entre tempo de tela e fadiga mental.

Insights Obtidos
Através das visualizações, é possível identificar padrões como:

A correlação direta entre o uso de celular antes de dormir e a redução na pontuação de qualidade do sono.

Quais profissões apresentam os maiores picos de fadiga mental e estresse.

Este projeto foi desenvolvido para fins de estudo em Ciência de Dados e Engenharia de Dados.
