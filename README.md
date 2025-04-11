# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# FIAP Fase6_Enterprise_Challenge_Sprint2


## 👨‍🎓 Integrantes: 
- <a href="https://www.linkedin.com/in/amanda-fragnan-b61537255/" target="_blank">Amanda Fragnan RM 555684 </a>
- <a href="https://www.linkedin.com/in/cunhaandre/" target="_blank">Andre Cunha RM 560648</a>
- <a href="https://www.linkedin.com/in/gabriellehalasc/" target="_blank">Gabrielle Halasc RM 560147</a> 

## 👩‍🏫 Professores:
### Tutor(a)
- <a href="https://www.linkedin.com/in/lucas-gomes-moreira-15a8452a/">Lucas Gomes Moreira</a>
### Coordenador(a)
- <a href="https://www.linkedin.com/in/profandregodoi/">André Godoi</a>

## 📜 Descrição

Projeto: Predição de Produtividade Agrícola com Modelos de Regressão

🎯 Objetivo Geral 

O projeto tem como finalidade desenvolver modelos preditivos capazes de estimar a produtividade agrícola do município de São José do Rio Preto, utilizando variáveis ambientais e históricas, como o NDVI médio (Índice de Vegetação por Diferença Normalizada) e a área colhida. A iniciativa busca apoiar a análise de safras e subsidiar a tomada de decisões estratégicas no setor agrícola, com foco em previsibilidade e eficiência.

## ⚙️ Funcionalidades da Solução

🔄 Processamento de Dados Agrícolas e Ambientais
Integração e tratamento de múltiplas fontes de dados, incluindo séries históricas de produção agrícola, NDVI médio e área colhida;

Padronização de formatos, conversão de datas e agregações temporais por ano.

📈 Análise Exploratória
Realização de análises estatísticas e visuais para identificar tendências, outliers e relações entre as variáveis;

Avaliação da correlação entre os indicadores e a variável-alvo (produção total).

🧠 Modelagem Preditiva com Inteligência Artificial
Implementação e comparação de dois algoritmos de regressão supervisionada: Regressão Linear e Random Forest Regressor;

Aplicação de técnicas de validação cruzada (5-fold) para assegurar robustez, minimizar overfitting e garantir a generalização dos modelos.

## 📊 Documentação do Processo de Preparação dos Dados

A etapa de preparação de dados envolveu:

Leitura e análise de três bases: dados_hist.xlsx, satveg_planilha.xlsx e Area_Colhida_Lavouras_Permanentes.xlsx;

Conversão e padronização de campos temporais, agregando os dados por ano;

Cálculo do NDVI médio anual por município;

Consolidação da produção total de lavouras permanentes por período;

Junção das bases através da variável comum Ano, originando o dataset df_final, com as variáveis principais: NDVI_Medio, Area_Colhida e Total_Produzido.

## 📌 Justificativa da Escolha das Variáveis

As variáveis foram selecionadas com base na sua relevância agronômica e estatística:

NDVI_Medio: Indicador remoto amplamente utilizado para representar a densidade e vigor da vegetação, sendo um reflexo direto da saúde das plantações.

Area_Colhida: Reflete o esforço produtivo, estrutura e escala das operações agrícolas.

Ambas mostraram forte correlação com a variável-alvo, Total_Produzido, durante a análise exploratória, justificando sua inclusão na modelagem.

## 🧠 Justificativa do Modelo e Lógica Preditiva

Foram aplicados dois modelos supervisionados:

Random Forest Regressor
Modelo de aprendizado de máquina baseado em ensemble de árvores de decisão. Apresenta boa performance em problemas com relações não-lineares e variáveis interdependentes.

Regressão Linear
Modelo estatístico tradicional, escolhido como baseline. Permite interpretação direta dos coeficientes e facilita o entendimento das contribuições individuais das variáveis.

Ambos foram treinados com divisão 80/20 (treino/teste) e avaliados com validação cruzada para melhor estimativa de desempenho.

## 🖼️ Prints das Análises Exploratórias

📌 Imagem NDVI

![NDVI_PNG_GRAFICO](https://github.com/user-attachments/assets/29525008-f985-4e27-b32b-e5efe12bb7a0)

📈 NDVI vs Área Colhida

![image](https://github.com/user-attachments/assets/a17f155c-e49c-4222-b97f-3b9068ddb10c)
 
📉 Correlação NDVI x Produção Total

![image](https://github.com/user-attachments/assets/f740d1a1-6672-4ba0-a2ce-b7bf94a0ce8e)

📦 Boxplots

![image](https://github.com/user-attachments/assets/002b0fd6-5918-4624-b43f-399068ea14f1)

📉 Random Forest - Real vs Previsto

![image](https://github.com/user-attachments/assets/cf938423-3048-416b-9574-054a0b7e414e)

📉 Regressão Linear - Real vs Previsto

![image](https://github.com/user-attachments/assets/ecd18dfb-5d0b-43a1-af30-465a3f87ef24)


## 📊 Justificativa Técnica e Métricas

Regressão Linear
R²: 0.576 → Explica 57,6% da variância da produção.

MSE: Valor médio do erro quadrático.

Erro Percentual Médio: 25,66%

Gráfico Real vs Previsto:


Random Forest
R²: 0.463 → Explica 46,3% da variância.

Erro Percentual Médio: 28,86%

Gráfico Real vs Previsto:


## 🔁 Validação Cruzada 
Modelo	R² Médio	Observação
Random Forest	-0.034	Indica overfitting
Regressão Linear	-0.221	Alta variância entre folds
A dispersão elevada e os R² negativos apontam para problemas de generalização, possivelmente ligados ao tamanho reduzido da amostra e desequilíbrio temporal ou espacial.

## ✅ Conclusão

A Regressão Linear apresentou desempenho mais consistente frente ao modelo de Random Forest, conforme os resultados obtidos no conjunto de teste:

R² de 0.576, revelando que aproximadamente 57,6% da variância na produtividade agrícola pôde ser explicada pelas variáveis selecionadas.
Erro percentual médio de 25,66%, indicando um desvio relativo moderado entre os valores previstos e observados.
O modelo de Random Forest, apesar de sua natureza não paramétrica e capacidade de modelar relações não lineares, apresentou:

R² de 0.463, com uma explicação menor da variabilidade dos dados.
Erro percentual médio de 28,86%, sugerindo uma menor precisão na escala produtiva analisada.
A validação cruzada com 5 folds evidenciou um ponto crítico: ambos os modelos apresentaram valores negativos de R² médio, com elevada dispersão nos scores individuais. Isso aponta para sérios problemas de generalização, provavelmente decorrentes de overfitting, baixa representatividade dos dados amostrais e desbalanceamentos temporais ou espaciais na base utilizada.

## 📌 Implicações Práticas e Limitações

Os modelos desenvolvidos apresentam viabilidade inicial para a construção de sistemas preditivos de produtividade com uso de variáveis remotas (como NDVI) e estruturais (como área plantada ou colhida). No entanto, os resultados também deixam claro que tais modelos, em seu estado atual, não estão prontos para subsidiar decisões críticas no contexto da gestão agrícola, principalmente em escalas locais.

As principais limitações encontradas ao longo do projeto não estão apenas relacionadas ao desempenho algorítmico, mas à qualidade, disponibilidade e granularidade dos dados. Uma das barreiras mais significativas observadas foi a dificuldade de acesso a dados agrícolas com recorte municipal e histórico consistente.

A maioria das bases públicas disponíveis concentra-se em níveis agregados por estado ou país, e normalmente segmenta os dados por tipo de cultura em relatórios e tabelas separadas, tornando inviável uma visão consolidada do volume produtivo de um determinado município ao longo do tempo.

Apesar de o IBGE — por meio de iniciativas como o PAM (Produção Agrícola Municipal) e o LSPA (Levantamento Sistemático da Produção Agrícola) — se aproximar desse ideal, ambos os levantamentos apresentam lacunas importantes, como ausência de cruzamento entre culturas e municípios e deficiências na qualidade e estruturação dos dados. Isso limita fortemente a aplicação de modelos preditivos mais robustos em escala local, afetando não apenas a modelagem estatística, mas também a possibilidade de análises multivariadas e históricas com acurácia confiável.

## 🔚 Encerramento

O presente estudo representa um primeiro passo em direção à modelagem inteligente da produção agrícola no Brasil, evidenciando tanto o potencial técnico da ciência de dados nesse domínio, quanto os desafios estruturais ainda existentes no acesso e padronização de informações agrícolas em nível municipal.

Avançar nesse tipo de iniciativa requer investimento contínuo em dados abertos, interoperabilidade de sistemas e digitalização do campo — pilares fundamentais para uma agricultura mais sustentável, resiliente e orientada por dados.

## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- <b>.gitignore</b>: Nesta pasta ficarão os  arquivos ou pastas devem ser ignorados pelo Git durante os commits

- FiapEnterprise2.ipynb: Notebook Jupyter com a implementação principal do projeto.

- LEIA-ME.md: Documento que funciona como um guia geral do projeto, apresentando seus objetivos, estrutura, funcionamento e instruções de uso. Este é o arquivo de leitura inicial para novos usuários.

- assets/NDVI_PNG_GRAFICO.png: Imagem gerada durante o projeto, destinada a armazenar um gráfico.

- Area_Colhida_Lavouras_Permanentes.xlsx, dados_hist.xlsx, satveg_planilha.xlsx: Planilhas com os dados históricos e atuais utilizados para análise e geração dos modelos e visualizações no projeto.

## 🔧 Como executar o código

1. Clonar o repositório

Primeiro, faça o clone deste repositório localmente usando o Git:

git clone https://github.com/AmandaFragnan/Enterprise_Challenge_Sprint2.git

2. Instalar dependências

Certifique-se de ter todas as dependências instaladas. Se estiver usando Python, você pode instalar os pacotes necessários com:

pip install -r requirements.txt

3. Executar o código
   
Dependendo da linguagem e estrutura do projeto, execute o código usando o comando apropriado. Para Python, por exemplo:

python main.py

## Historico de lançamentos

- <b> 0.1.0 - 11/04/2025<b>

  
## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>
