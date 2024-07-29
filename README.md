# CIFAR 10 com Redes Neurais Convolucionais

Neste trabalho desenvolveremos um projeto de Aprendizado de Máquina Supervisionado utilizando Redes Neurais Artificiais como modelo de referência.

## Objetivos

São os objetivos desse trabalho as seguintes etapas:

1. Coleta e preparação de dados;

2. Análise exploratória da base de dados;

3. Determinação da tarefa de Aprendizado de Máquina;

4. Determinação da abordagem de validação cruzada a ser adotada e das métricas de desempenho a serem aferidas, com justificativa que corroborem as escolhas efetuadas;

5. Elaboração de uma grade de busca de modelos, parâmetros e hiperparâmetros nas Redes Neurais Artificiais;

6. Treinamento e teste dos modelos;

7. Análise qualitativa e quantitativa de desempenho dos modelos avaliados.

## Análise exploratória 

A base utilizada para o desenvolvimento do projeto foi o **CIFAR 10** que consiste num dataset com 60 mil imagens de dimensões 32x32 distribuídos em 10 classes. As 10 classes são: aviões, carros, pássaros, gatos, veados, cães, sapos, cavalos, navios e camiões.

Por padrão o dataset já está dividido da seguinte forma: 50 mil imagens de treinamento e 10 mil imagens para teste

A seguir uma visão geral do dataset:

![](./imagens/img1.jpg)

Foi feita uma leitura no código Python do dataset e esta é uma imagem que pode ser visualizada:

![](./imagens/img2.jpg)

## Determinação da tarefa de Aprendizado de Máquina
A determinação da tarefa de aprendizado de máquina é crucial para o sucesso do projeto. Neste trabalho, o objetivo é classificar imagens com base em dados previamente coletados, o que configura a tarefa como classificação, uma forma de aprendizado supervisionado. Isso significa que o modelo aprenderá a partir de um conjunto de imagens rotuladas, associadas a categorias específicas, para prever a categoria de novas imagens.

## Validação Cruzada
A abordagem da validação cruzada usada neste projeto deveu-se a utilização da ferramenta StratifiedKFold do Scikit-Learning onde o número de k-folds especificado foi igual a 10. Os parâmetros testados foram os mesmo da criação do modelo.
A média dos 10 resultados que foi realizado deu um valor de 76.456% de acurácia.

## Grade de Busca

Na grade de busca foram experimentados dois tipos diferentes de otimizadores, assim como no tamanho da forma (batch) e na quantidade de épocas, a fim de encontrar uma combinação que apresentasse melhores métricas de teste.


## Gráficos

Os gráficos mostram o desempenho das redes em termos de acurácia e desvio padrão. Lembrando que os gráficos de acurácias foram ordenados para melhor visibilidade e cada
valor da abscissa no gráfico de desvio padrão corresponde à abscissa no gráfico de acurácias. Pode-se perceber que modelos se adaptam melhor aos dados que apresentam acurácias maiores. E para as mesmas redes, há desvios padrão de validação cruzada tendenciodamente mais baixos, indicando consistência.  
