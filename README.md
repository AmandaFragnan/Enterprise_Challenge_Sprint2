
# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# FIAP Fase_6_Enterprise_Challenge_Sprint_2


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

• Objetivo Geral
Este projeto tem como objetivo prever a produtividade agrícola de São José do Rio Preto com base em variáveis ambientais e históricas, como NDVI médio (índice de vegetação) e área colhida. A proposta visa fornecer um modelo preditivo que auxilie na análise de safras e na tomada de decisão no setor agrícola

## ⚙️ Funcionalidades da Solução

Processamento de Dados Ambientais e Agrícolas:
Integração e transformação de dados históricos de área colhida, NDVI médio e produção de lavouras permanentes.

Análise Exploratória Detalhada:
Análise visual e estatística para identificação de tendências, outliers e correlações entre as variáveis envolvidas.

Modelagem Preditiva com IA:
Implementação e comparação de modelos de Regressão Linear e Random Forest para previsão da produção agrícola.

Validação Cruzada:
Aplicação de validação cruzada (5-fold) para verificar a robustez dos modelos e sua capacidade de generalização.

## 📊 Documentação do Processo de Preparação dos Dados

A preparação envolveu:

Leitura de três conjuntos de dados (dados_hist.xlsx, satveg_planilha.xlsx, Area_Colhida_Lavouras_Permanentes.xlsx);

Conversão de datas e agregação por ano;

Cálculo do NDVI médio anual;

Soma da produção total de todas as lavouras permanentes;

Junção final entre os datasets com base no ano (Ano), formando o dataset df_final com 3 variáveis principais: NDVI_Medio, Area_Colhida e Total_Produzido.

## 📌 Justificativa da Escolha das Variáveis

As variáveis selecionadas para a modelagem foram:

NDVI_Medio: Representa a densidade da vegetação e saúde das plantações.

Area_Colhida: Indica o esforço produtivo em campo, refletindo capacidade de colheita.

Essas variáveis foram escolhidas por sua relevância direta na formação do volume total produzido e por apresentarem boa correlação com o alvo (Total_Produzido) na análise exploratória.

## 🧠 Justificativa do Modelo e Lógica Preditiva
Dois modelos supervisionados foram aplicados:

Random Forest Regressor
Modelo baseado em múltiplas árvores de decisão. Capaz de capturar relações não-lineares. Utilizado para avaliar a complexidade do problema.

Regressão Linear
Modelo estatístico mais simples, útil para estabelecer uma base comparativa e interpretar diretamente os coeficientes preditivos.

Ambos os modelos foram treinados com divisão de dados 80/20 (treino/teste) e posteriormente avaliados por validação cruzada.

## 🖼️ Prints das Análises Exploratórias

📌 Imagem NDVI

📈 NDVI vs Área Colhida

📉 Correlação NDVI x Produção Total

📦 Boxplots

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


## 🔁 Validação Cruzada (5-fold)
Modelo	R² Médio	Observação
Random Forest	-0.034	Indica overfitting
Regressão Linear	-0.221	Alta variância entre folds
A dispersão elevada e os R² negativos apontam para problemas de generalização, possivelmente ligados ao tamanho reduzido da amostra e desequilíbrio temporal ou espacial.

## ✅ Conclusão

A Regressão Linear apresentou desempenho mais consistente para este conjunto de dados limitado. Apesar da simplicidade, ela superou o Random Forest tanto em explicabilidade quanto em desempenho geral nos testes. Sugere-se aumentar a base de dados e considerar variáveis externas (precipitação, temperatura, solo) para futuras melhorias.


## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- <b>.gitignore</b>: Nesta pasta ficarão os  arquivos ou pastas devem ser ignorados pelo Git durante os commits

- <b>PYTHON_E_ALEM</b>: aqui estão os arquivos com o codigo python e ajuste para conexão do banco em nuvem.

- <b>requirements.txt</b>: Lista  com todas as dependências ou bibliotecas necessárias para que o projeto funcione corretamente.

- <b>README.md</b>: arquivo que serve como guia e explicação geral sobre o projeto (o mesmo que você está lendo agora).

- <b>assets</b>: aqui estão os arquivos relacionados a elementos não-estruturados deste repositório, como imagens.

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
