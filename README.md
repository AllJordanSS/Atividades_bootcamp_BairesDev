# Atividade 2 - Transfer Learning: Classificação de Imagens (Gato vs Coelho)

Este projeto tem como objetivo aplicar Transfer Learning para classificar imagens de gatos e coelhos utilizando uma rede neural pré-treinada (VGG16) do Keras.

## Objetivo
Desenvolver um modelo capaz de distinguir entre imagens de gatos e coelhos, utilizando um dataset próprio e técnicas de Transfer Learning para aproveitar o conhecimento de redes treinadas em grandes bases de dados (ImageNet).

## Metodologia
- **Dataset:**
	- As imagens foram coletadas online e organizadas nas pastas `classes/bunny` e `classes/cat`.
	- O dataset contém 488 imagens, divididas em treino (70%), validação (15%) e teste (15%).
- **Pré-processamento:**
	- Redimensionamento das imagens para 224x224 pixels.
	- Normalização dos dados e conversão dos rótulos para one-hot encoding.
- **Transfer Learning:**
	- Utilização do modelo VGG16 pré-treinado com ImageNet.
	- Adição de uma nova camada de classificação (softmax) para distinguir entre as duas classes.
	- Congelamento dos pesos das camadas originais, treinando apenas a nova camada.
- **Treinamento:**
	- 10 épocas, batch size de 128.
	- Otimizador Adam e função de perda categorical_crossentropy.

## Resultados
- **Acurácia final no conjunto de teste:** ~71%
- O modelo foi capaz de classificar corretamente imagens nunca vistas de gatos e coelhos.
- Exemplo de predição:
	- Probabilidade para gato: 0.83
	- Probabilidade para coelho: 0.17

## Como executar
1. Certifique-se de ter as dependências do Keras e TensorFlow instaladas.
2. Organize as imagens nas pastas `classes/bunny` e `classes/cat`.
3. Execute o notebook `Atividade_Tranfer_learning.ipynb` para treinar e testar o modelo.

## Link do notebook no Google Colab
[Atividade_Tranfer_learning.ipynb no Colab](https://colab.research.google.com/drive/1_q2o2E_3Spz-YyrGAvoJldnqxHM5NF7d?usp=sharing)

## Autor
All Jordan S. Souza

---
Projeto desenvolvido para o Bootcamp BairesDev.
# Dataset-bunny_cat
Dataset criado para atividades do Bootcamp de Machine Learning pela BairesDev e DIO
