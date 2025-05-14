# Primeiros Princípios da Visão Computacional

Os **Primeiros Princípios da Visão Computacional** são os fundamentos teóricos e práticos que sustentam os sistemas que interpretam imagens e vídeos para extrair informações do mundo visual. Abaixo, apresento uma estrutura organizada com os principais conceitos:

***

### 🧠 Primeiros Princípios da Visão Computacional

#### 1. **Formação da Imagem**

* **Modelo de Câmera Pinhole**: Representa como um ponto 3D do mundo real é projetado em uma imagem 2D.
* **Projeção Perspectiva**: Transforma coordenadas 3D em coordenadas 2D no plano da imagem.
* **Calibração de Câmera**: Determina os parâmetros intrínsecos (foco, centro óptico) e extrínsecos (posição e orientação da câmera).

#### 2. **Geometria Computacional**

* **Transformações 2D e 3D**: Matrizes de rotação, translação e escalonamento para manipulação de objetos e cenas.
* **Epipolaridade e Estéreo Visão**: Relação entre dois pontos de vista — base para reconstrução 3D.
* **Homografia**: Transformação entre planos em diferentes perspectivas.

#### 3. **Processamento de Imagem**

* **Pré-processamento**: Filtragem (Gaussian blur, sharpening), equalização de histograma.
* **Detecção de Bordas**: Operadores como Sobel, Canny, Laplaciano.
* **Segmentação**: Separação da imagem em regiões significativas (thresholding, clustering, watershed).

#### 4. **Reconhecimento de Padrões**

* **Detecção de Características**: Pontos-chave (SIFT, SURF, ORB) usados para rastreamento e reconstrução.
* **Descritores**: Representações compactas para comparação de padrões visuais.
* **Classificação**: SVM, Árvores de Decisão, Redes Neurais Convolucionais (CNNs).

#### 5. **Reconstrução 3D**

* **Structure from Motion (SfM)**: Usa múltiplas imagens para estimar estrutura 3D e movimento da câmera.
* **Photometric Stereo**: Usa variações de iluminação para reconstruir a geometria de superfícies.
* **Stereo Matching**: Combina imagens estéreo para estimar profundidade.

#### 6. **Modelos de Cor e Iluminação**

* **Espaços de Cor**: RGB, HSV, Lab — usados para representar e manipular cores.
* **Reflexão e Sombreamento**: Modelos como Lambertiano e Phong explicam como a luz interage com as superfícies.
* **Constância de Cor**: Capacidade de perceber as cores de objetos como constantes sob diferentes condições de iluminação.

#### 7. **Aprendizado de Máquina e Deep Learning**

* **CNNs (Redes Neurais Convolucionais)**: Arquiteturas como LeNet, AlexNet, ResNet são pilares do reconhecimento visual moderno.
* **Detecção de Objetos**: YOLO, SSD, Faster R-CNN.
* **Segmentação Semântica e por Instância**: U-Net, Mask R-CNN.

***

