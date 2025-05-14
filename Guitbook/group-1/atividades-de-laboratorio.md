---
description: Visão Computacional
---

# ATIVIDADES DE LABORATÓRIO

### Introdução ao processamento de imagem

Uma biblioteca Python comumente usada para trabalhar com elementos da fotogrametria é a biblioteca OpenCV (Open Source Computer Vision Library). O OpenCV é uma biblioteca de código aberto que fornece várias funções e algoritmos para processamento de imagens e visão computacional, incluindo recursos específicos para fotogrametria.

Com o OpenCV, você pode realizar várias tarefas relacionadas à fotogrametria, como:

1. Detecção de pontos de interesse em imagens.
2. Correspondência de pontos-chave entre imagens.
3. Estimativa de homografia e matriz fundamental.
4. Estimativa de pose de câmera.
5. Reconstrução 3D a partir de múltiplas imagens.

Além do OpenCV, também existem outras bibliotecas que podem ser úteis para tarefas específicas de fotogrametria:

1. NumPy: Uma biblioteca fundamental para computação científica em Python, que pode ser usada para manipular matrizes e realizar cálculos numéricos necessários em fotogrametria.
2. SciPy: Uma biblioteca que fornece várias funcionalidades úteis para processamento de sinais e imagens, como filtragem, interpolação e transformadas.
3. Matplotlib: Uma biblioteca de visualização em Python que pode ser usada para exibir imagens, gráficos e resultados de reconstruções 3D.

Essas bibliotecas são amplamente utilizadas na comunidade de fotogrametria e podem ajudar você a realizar várias tarefas nessa área. É importante ressaltar que a fotogrametria é um campo amplo e complexo, e dependendo do seu projeto específico, pode ser necessário usar ferramentas e bibliotecas adicionais.

Por favor, note que as informações fornecidas acima são baseadas no conhecimento disponível até a data de corte do meu treinamento em setembro de 2021. É possível que tenham sido desenvolvidas novas bibliotecas ou atualizações desde então. Recomenda-se sempre verificar as fontes atualizadas e a documentação oficial das bibliotecas para obter as informações mais recentes sobre fotogrametria em Python.

### **Objetivo:**

Aprender os conceitos elementares de processamento de imagem (importação, análise, manipulação e saída) e operações que podem ser realizadas com imagens. Neste curso os alunos desenvolveram programas básicos de processamento de imagens utilizando bibliotecas de visão computacional.

**Tópicos:**

* Conceitos de processamento de imagem
* O que é uma imagem
  * Matriz de pixels
  * Cores e canais
  * Formatos
  * Domínios
  * Amostragem
  * Quantização
* Níveis de processamento
* baixo-nível: operações primitivas (filtro de ruídos e tratamento de contraste)
* Nível-médio (segmentação e classificação)
* Alto-nível (tarefas de cognição)
* Importar imagem através de uma ferramentas/API
* Analisar/manipular imagens usando bibliotecas
  * OpenCV para Python
  * Scikit-image

**Bibliografia:**

Walt, S. van der, Schönberger, J.L., Nunez-Iglesias, J., Boulogne, F., Warner, J.D., Yager, N., Gouillart, E., Yu, T., 2014. scikit-image: image processing in Python. PeerJ 2, e453.

Shilkrot, R., Escriva, D.M., 2018. Mastering OpenCV 4: A comprehensive guide to building computer vision and image processing applications with C++, 3rd Edition. Packt Publishing.

## CURSO RÁPIDO DE PYTHON PARA INICIANTES COM GOOGLE COLAB

{% embed url="https://www.youtube.com/playlist?list=PLCAhGm8nJ9CDV30W-0q8K4xzmGHIXnW6h" %}

### Roteiro para Trabalhar com Python

{% embed url="https://colab.research.google.com/drive/1UeFuFpMJ9-90ZwY30RkstDjU3EU-fr53#scrollTo=2Gfxp-pM2re6" %}

## Introdução ao Processamento Digital de Imagens

{% embed url="https://colab.research.google.com/drive/1eKAwY7Y1RYtWptIGPwfZr1nhNYkZX8N4?usp=sharing" %}

#### &#x20;<a href="#convertendo-imagens" id="convertendo-imagens"></a>

#### CONVERTENDO IMAGENS <a href="#convertendo-imagens" id="convertendo-imagens"></a>

* Usando o interpretador Python, abra e exiba imagens de exemplo.
* Usando a função _imwrite_ grave a imagem "encripted.png" no formato PPM (texto).

#### DESAFIO DE DECODIFICAÇÃO <a href="#desafio-de-decodifica-o" id="desafio-de-decodifica-o"></a>

* Abra o arquivo ppm do exercício anterior num editor de texto e analise o formato do arquivo. Contabilize quantas linhas são usadas para cabeçalho da imagem.
* Crie um script em Python para ler todos os números num arquivo e convertê-los em caracteres segundo a tabela ASCII usando a função _chr_.
* Decodifique o arquivo ppm com esse _script_.

#### CANAIS DE COR <a href="#canais-de-cor" id="canais-de-cor"></a>

* Crie um _script_ para separar e exibir os canais de cor de uma imagem.
* Crie um _script_ para fusionar canais de cor (bandas) de uma mesma imagem.
* Crie um _script_ capaz de trocar a ordem dos canais de cor numa imagem.
* Crie um _script_ capaz de inverter os valores nos canais de cores de uma imagem.

#### TRANSFORMAÇÕES GEOMÉTRICAS <a href="#transforma-es-geom-tricas" id="transforma-es-geom-tricas"></a>

* Crie um _script_ para reduzir $$4×$$4× o tamanho de uma imagem.
* Crie um _script_ para rotacionar $$45o$$45uma imagem.
* Crie um _script_ para colar duas imagens lado a lado.
* Crie um _script_ para espelhar uma imagem usando a função _warpAffine_.
* Crie um _script_ que desloque os _pixels_ de uma imagem segundo uma senoide.
