# Criar CNN - Convolutional Neural Network para identificacão de cones com TensorFlow e Keras
 - Desde a instalacao do Anaconda ao Treino e Predicao da rede ( VGG16 )

## Index

<!-- Table of contents generated by http://tableofcontent.eu/ -->
- [1 - Install Anaconda 5.1](#1-install-anaconda)
- [2 - Linux Ubuntu 16](#2-linux-ubuntu-16)
- [3 - Python para Windows](#3-python-para-windows)
- [4 - Instalando o Cuda e Cudnn com suporte a GPU](#4-Install-CUDA-Cudnn-support-GPU)
- [5 - Cuda 8 GA2]
- [6 - PATH] 
- [7 - Instalando os pacotes necessários]
- [8 - Iniciando o jupyter notebook]
- [9 - Montando a Rede VGG 16]


- [Saving Remission Map Images](#saving-remission-map-images)
- [Splitting the Remission Map Images](#splitting-the-remission-map-images)
- [Rules for Ground Truth Annotations on Remission Map Images](#rules-for-ground-truth-annotations-on-remission-map-images)

## 1-Install Anaconda
Acessar o site http://anaconda.com/download
Fazer o Download da versao respectiva ao seu SO e também a versao do Python

## 2-Linux Ubuntu 16
Python 3.6 https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh Python 2.7 https://repo.continuum.io/archive/Anaconda2-5.0.1-Linux-x86_64.sh Abrir um terminal, acessar o local onde o arquivo foi baixado e seguir com o seguinte comando bash ~/Downloads/Anaconda3-5.0.1-Linux-x86_64.sh (versao 3.6 do Python)

## 3-Python para Windows
Python 3.6 https://repo.continuum.io/archive/Anaconda3-5.0.1-Windows-x86_64.exe Python 2.7 https://repo.continuum.io/archive/Anaconda2-5.0.1-Windows-x86_64.exe Para instalar é só dar um duplo clique no instalador e seguir

# A partir deste momento vou cobrir os passos apenas para o linux como sistema operacional

## 3 - Install CUDA e Cudnn com suporte a GPU
Caso queira rodar os treinamentos com recursos de GPU é necessário instalar os pacotes CUDA e Cudnn as versoes destes sao muito importantes para que tudo funcione corretamente como até o momento a ultima versao disponível do tensorflow é a 1.4 vou usar as versões de Cuda e Cudnn que a pagina recomenda como versões suportadas lembrando que a placa de video deve ser compatível com cuda e ter os drivers da nvidia instalados









The Road Mapper module manages the *map_type* CARMEN_ROAD_MAP_v (prefix character 'r'), the data structure *road_prob* and the map server message CARMEN_MAP_SERVER_ROAD_MAP_NAME. Each cell in a road gridmap contains the following data:
```c
 typedef struct				/* Probabilities of a pixel in the road map: range(0, 0xffff) */
 {
   unsigned short off_road;		/* Probability of being off the road */
   unsigned short solid_marking;	/* Probability of being in a lane solid marking */
   unsigned short broken_marking;	/* Probability of being in a lane broken marking */
   unsigned short lane_center;		/* Probability of being at the center of a lane */
 } road_prob;
```
The following color code is used for displaying a road map:
  - ![#ffffff](data/20x20_bg_white_border_gray.png) RGB(255, 255, 255) = off the road
  - ![#ff0000](https://placehold.it/20x20/ff0000/?text=+) RGB(255, 000, 000) = solid marking
  - ![#0000ff](https://placehold.it/20x20/0000ff/?text=+) RGB(000, 000, 255) = broken marking
  - ![#00ff00](https://placehold.it/20x20/00ff00/?text=+) RGB(000, 255, 000) = center of a lane


