# Estéreo Visão



***

### 📦 Requisitos

Instale o OpenCV:

```bash
pip install opencv-python opencv-contrib-python
```

***

### 📁 Estrutura Esperada de Arquivos

Tenha duas imagens estéreo (exemplo: `left.png` e `right.png`) no mesmo diretório do script. Se quiser, posso enviar imagens de exemplo.

***

### 🧪 Código Python: Estéreo Visão com OpenCV

[https://colab.research.google.com/drive/1X9OzfxWR6BsL3kXUghZBUX9uuUUgZYZy?usp=sharing](https://colab.research.google.com/drive/1X9OzfxWR6BsL3kXUghZBUX9uuUUgZYZy?usp=sharing)

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Carregar as imagens estéreo
img_left = cv2.imread('left.png', cv2.IMREAD_GRAYSCALE)
img_right = cv2.imread('right.png', cv2.IMREAD_GRAYSCALE)

# Verificar se as imagens foram carregadas
if img_left is None or img_right is None:
    raise IOError("Imagens não encontradas. Certifique-se de que 'left.png' e 'right.png' existem.")

# Criar o objeto estéreo usando o algoritmo StereoBM
stereo = cv2.StereoBM_create(numDisparities=64, blockSize=15)

# Calcular a disparidade
disparity = stereo.compute(img_left, img_right)

# Normalizar para visualização
disparity_normalized = cv2.normalize(disparity, None, alpha=0, beta=255, norm_type=cv2.NORM_MINMAX)
disparity_normalized = np.uint8(disparity_normalized)

# Mostrar resultado
plt.figure(figsize=(10, 4))
plt.subplot(1, 3, 1)
plt.title("Imagem Esquerda")
plt.imshow(img_left, cmap='gray')

plt.subplot(1, 3, 2)
plt.title("Imagem Direita")
plt.imshow(img_right, cmap='gray')

plt.subplot(1, 3, 3)
plt.title("Mapa de Disparidade")
plt.imshow(disparity_normalized, cmap='jet')
plt.colorbar()
plt.tight_layout()
plt.show()
```

***

### 🧠 Explicação

* `StereoBM_create()`: Algoritmo block matching (rápido, mas sensível a ruído);
* `numDisparities`: Intervalo máximo de disparidade. Deve ser múltiplo de 16;
* `blockSize`: Tamanho do bloco para comparação (ímpar, ex: 15);
* `normalize()`: Torna o mapa legível como imagem 2D.

***

### 🔄 Possíveis Extensões

* Substituir por **StereoSGBM\_create()** para maior precisão;
* Aplicar calibração com parâmetros reais;
* Estimar profundidade com fórmula $$Z=f⋅BdZ = \frac{f \cdot B}{d}.$$

***

Deseja que eu gere imagens de exemplo para teste com esse código?
