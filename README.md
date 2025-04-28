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

## 🖼️ Prints dos resultados

📌 Imagem trator

![image](https://github.com/user-attachments/assets/49645ecf-8c44-483c-92ec-bc45f1d04987)


📌 Imagem casa

![image](https://github.com/user-attachments/assets/b6fda0f6-67dd-45ee-8025-db4a7c5a8c14)

 


## 📊 Link video

https://youtu.be/i6o_5E1ckbo


## Historico de lançamentos

- <b> 0.1.0 - 28/04/2025<b>

  
## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>
