# Towards Real-World Blind Face Restoration with Generative Facial Prior
## Resumo
Embora muitas tentativas tenham sido feitas na superresolução cega para restaurar imagens de baixa resolução com degradações complexas e desconhecidas, elas ainda estão longe de abordar imagens degradadas do mundo real em geral,Neste trabalho, propomos a utiçização GFP-GAN que aproveita antecedentes ricos e diversos encapsulados em um GAN de face pré-treinado para restauração de face cega. Este Generative Facial Prior (GFP) é incorporado ao processo de restauração
facial por meio de camadas de transformação de recursos espaciais, o que permite que nosso método alcance um bom equilíbrio entre
realidade e fidelidade.  
## Introdução
A tarefa altamente desafiadora de estimar uma imagem de alta resolução (HR) a partir de sua contraparte de baixa resolução (LR) é conhecida como super-resolução (SR).Quando tiramos uma foto com nossos celulares, as fotos podem ter várias degradações ou ruidos, como por exemplo desfoque da câmera, ruído do sensor, artefatos de nitidez e compactação JPEG, edições e carregamento em  mídias sociais, o que gera mais compressão e ruídos que são imprevisíveis. A  restauração cega de imagens é restaurar uma imagem degradada sem usar informação da imagem real ou da função de degradação, No entanto, entradas de qualidade muito baixa podem dificultar esse processo.

## Objetivo
Neste estudo, aproveitamos Prioridade facial generativa (GFP) para restauração de rosto cego no mundo real, que consiste em gerar uma imagem de alta resolução (HR) a partir de sua contraparte de baixa resolução (LR), ou seja, dada uma imagem X que sofre uma degradação desconhecida, o objetivo é estimar uma imagem de alta qualidade ŷ, que é o mais semelhante possível à imagem da verdade fundamental y, em termos de realidade e fidelidade.
## Outras Soluções
O GFP-GAN foi comparado com vários métodos de restauração de rosto de última geração como HiFaceGAN , DFDNet e PSFRGAN. 
![PDI](https://user-images.githubusercontent.com/32283837/133941372-1a8bc17d-0f83-4ce0-9041-f372acf47a19.png)
Também foi comparado com métodos de restauração de imagem: RCAN , ESRGAN  e DeblurGANv2
![PDI2](https://user-images.githubusercontent.com/32283837/133941385-1fa848cf-0ed2-4d4f-a824-d88c1281bc6b.png)

## Metodologia
O GFP-GAN é composto por um módulo de remoção de degradação (UNet) e um GAN de face pré-treinado (Style-GAN2 ), Eles são interligados por um mapeamento de código latente e várias camadas Channel-Split Spatial Feature Transform (CS-SFT).Especificamente, o módulo de remoção de degradação é projetado para remover degradação complicada e extrair dois tipos de recursos:
1. Características latentes
2. Recursos espaciais de multi-resolução
As características latentes são usadas para mapear a imagem de entrada para o código latente mais próximo no StyleGAN2  as  características espaciais  são usados para modular os recursos do StyleGAN2.
### O objetivo de aprendizagem de treinar o GFP-GAN consiste em: 
* Perda de reconstrução que restringe os resultados ŷ perto da verdade fundamental y.
* Perda adversária para restaurar texturas realistas
* Perda de componente facial proposta para melhorar ainda mais os detalhes faciais.
* Perda de preservação de identidade.

## Testes Particulares
![1](https://user-images.githubusercontent.com/32283837/133941083-536b88e4-a33c-4330-bc25-68680cc7725d.png)
![2](https://user-images.githubusercontent.com/32283837/133941124-f25ec68f-3ddc-4f35-a1e9-9c78840c2186.png)
![3](https://user-images.githubusercontent.com/32283837/133941181-1e4ee2a9-4cd5-45d9-a161-08ba729056bc.png)

## Conclusão
As comparações demonstram a grande capacidade do GFP-GAN na restauração da face da articulação e no aprimoramento da cor para imagens do
mundo real, superando algumas técnicas,  permitindo-nos alcançar um bom equilíbrio entre realidade e fidelidade
## Referências
1.<https://paperswithcode.com/paper/real-esrgan-training-real-world-blind-super#code>
2.<https://paperswithcode.com/paper/towards-real-world-blind-face-restoration>
3.<https://arxiv.org/abs/1809.00219>
