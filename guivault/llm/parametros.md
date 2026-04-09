+++
title = 'Parametros'
date = '2026-02-09'
+++


**Parâmetros** são valores utilizados para alimentar o processo de aprendizado de modelos de IA (especialmente em **Deep Learning**).

Existem três tipos principais: **Pesos**, **Vieses (Bias)** e **Hiperparâmetros**.

---

## Pesos
**Pesos** são valores numéricos atribuídos às entradas do modelo. Eles determinam o quanto cada entrada influencia a saída final da rede neural. Durante o treinamento, os pesos são ajustados automaticamente por algoritmos de otimização (como o gradiente descendente) para reduzir o erro das previsões.

**Exemplo:**  
Quando solicitamos ao GPT que produza um texto sobre **anfíbios**, palavras relacionadas ao tema recebem maior relevância estatística dentro do contexto gerado. Assim, termos associados ao assunto (como “sapo”, “rã” ou “habitat aquático”) tendem a influenciar mais o resultado do que palavras não relacionadas, como “leão”.

---

## Vieses (Bias)
Os **vieses** são valores adicionais somados às entradas ponderadas pelos pesos antes da função de ativação. Eles permitem que o modelo seja mais flexível, possibilitando que neurônios sejam ativados mesmo quando as entradas ponderadas são baixas. Isso aumenta a capacidade do modelo de aprender padrões complexos nos dados.

---

## Hiperparâmetros
**Hiperparâmetros** são parâmetros definidos externamente ao processo de treinamento e que controlam o comportamento do modelo e do algoritmo de aprendizado. Diferentemente dos pesos e vieses, eles **não são aprendidos automaticamente**, sendo definidos pelo desenvolvedor ou ajustados por técnicas de busca.

**Exemplos de hiperparâmetros:**
- Taxa de aprendizado (*learning rate*)
- Número de camadas da rede
- Número de neurônios por camada
- Tamanho do *batch*
- Número de épocas de treinamento
