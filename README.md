# Estimando a Trajetória Final de um Veículo com ICP

## Introdução ao Projeto

Uma tarefa que lidamos comumente é trabalhar com nuvens de pontos (point clouds). As point clouds são
dados que podem ser extraídos de formas diferentes: um par de câmeras (geometria estéreo), sensor LiDAR
(Light Detection And Ranging), sensores de profundidade e etc. Nessa tarefa, você receberá um conjunto de 30
scans extraídos de um LiDAR, estes dados são parte do KITTI DATASET. Utilize as point clouds de cada scan
para estimar a trajetória final do veículo, de forma que essa trajetória se inicie no primeiro scan. Para estimar
a trajetória percorrida pelo carro você deve usar o algoritmo Iterative Closest-Points (ICP). Contudo, você não
pode utilizar bibliotecas de terceiros para isso. Você deve fazer sua própria implementação do
algoritmo ICP. Em seu código, você deve mostrar que sua implementação está correta. Além disso, estamso
anexando a ground-truth que é um arquivo .npy, que pode ser aberto com a biblioteca NumPy. Ao carregá-lo,
você terá um array de tamanho (30, 4, 4). Cada linha, primeiro indice, representa uma matriz de
transformação em coordenadas homogêneas para cada uma das 30 posições do carro.
Link para o dataset - Link para a Ground-Truth
OBSERVAÇÕES:
- Use a ground-truth para comparar seu resultado. Com ela, você pode verificar se você está
chegando numa resposta próxima da realidade.
- Como descrito no corpo da questão, não é permitido usar bibliotecas que já possuam o algoritmo do
ICP implementado. Portanto, você não pode usar a implementação das bibliotecas como: Open3D ou
PCL. Contudo, você pode usar o algoritmo dessas bibliotecas como ground-truth para você verificar se
sua implementação está correta.
- Você pode usar bibliotecas como SciPy, NumPy, MatPlotLib.
- Caso você não tenha experiência com transformações de corpo rígido, veja essa playlist com
vídeo-aulas.
- É obrigatório que você demonstre o caminho percorrido, em todos os eixos (XYZ), pelo carro. Ou seja,
você deve mostrar um plot 3D da trajetória estimada pelo veículo. Ou, se possível, a matriz de
transformação final, em coordenadas homogêneas, do carro.
- Para carregar a nuvem de pontos, que estão nos arquivos .obj, você pode utilizar a biblioteca Trimesh.
Veja o exemplo abaixo de como carregar a point cloud:
import trimesh
point_cloud = trimesh.load(“000000_points.obj”).vertices

## Começando

### Google Colab Notebook:
1) Salve Uma Cópia no Google Drive do Notebook, à Partir da Url Abaixo, e Execute as Células do Notebook Sequencialmente Preferencialmente na GPU:

https://colab.research.google.com/drive/1ZZNTYuWXuv0Ueeo5mzIS2uysyEVm2324?usp=sharing

### Executar Localmente

1) Clone o Repositório, em Algum Local da Sua Máquina, Executando o Comando via Git:
git clone https://github.com/italopguimaraes/Point_Clouds-ICP.git

2) Com o Terminal Entre no Diretório Point_Clouds-ICP/ e Execute o Comando: jupyter notebook

3) Clique no Arquivo 'Prova_Daedalus_Questao_01.ipynb' e Abra no Navegador, Execute as Células Abaixo Sequindo as Instruções Deste Notebook.
