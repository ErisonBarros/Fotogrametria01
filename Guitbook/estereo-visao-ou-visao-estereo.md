# Estéreo Visão (ou Visão Estéreo)

A **Estéreo Visão** (ou **Visão Estéreo**) é um dos pilares da Visão Computacional e tem como objetivo **reconstruir a profundidade do mundo 3D** a partir de **duas ou mais imagens** capturadas de pontos de vista diferentes.

***

### 🎯 Conceito Fundamental

A estéreo visão se baseia no mesmo princípio da visão humana: temos **duas câmeras (olhos)** separadas por uma **distância conhecida** (base estereoscópica), e a diferença de posição de um objeto nas duas imagens (disparidade) é usada para estimar sua **distância**.

***

### 🧠 Etapas da Estéreo Visão

#### 1. **Captura de Imagens**

* Duas imagens são adquiridas com câmeras ligeiramente deslocadas horizontalmente.
* Idealmente, as câmeras são **calibradas** e alinhadas para que os eixos ópticos sejam paralelos.

#### 2. **Calibração das Câmeras**

* Determina os **parâmetros intrínsecos** (foco, centro da imagem) e **extrínsecos** (posição e orientação).
* Permite relacionar as imagens com o espaço 3D real.

#### 3. **Reta Epipolar**

* Para cada ponto em uma imagem, o ponto correspondente na outra imagem **deve estar sobre uma linha específica**, chamada **linha epipolar**.
* Reduz a busca de correspondência de 2D para 1D.

#### 4. **Correspondência Estéreo (Stereo Matching)**

* Encontra pares de pixels correspondentes nas duas imagens.
* Usa algoritmos como:
  * **Block Matching**
  * **Semi-Global Matching (SGM)**
  * **Deep Learning-based Matching** (por exemplo, PSMNet)

#### 5. **Cálculo da Disparidade**

*   A **disparidade** é a diferença horizontal entre as posições dos pontos correspondentes.

    d=xesquerda−xdireitad = x\_\text{esquerda} - x\_\text{direita}

#### 6. **Estimativa de Profundidade**

*   A profundidade $$Z$$de cada ponto pode ser estimada pela fórmula:

    $$Z=f⋅BdZ = \frac{f \cdot B}{d}$$

    Onde:

    * $$Z$$ = profundidade (distância do ponto até a câmera)
    * $$f$$ = distância focal da câmera
    * $$B$$ = baseline (distância entre as câmeras)
    * $$d$$= disparidade

***

### 📌 Aplicações

* Reconstrução 3D (ex: mapas de profundidade)
* Navegação de robôs/autônomos
* Medição de volume e distância
* Realidade aumentada
* Detecção de obstáculos em veículos

***

### 📷 Ilustração do Princípio

```
   Cena 3D
     |     \       ←   Ponto no mundo real
     |      \
Câmera E     Câmera D
Imagem E     Imagem D
 xE   ← d →   xD
```

