# Towards Real-World Blind Face Restoration with Generative Facial Prior
## Resumo
Embora muitas tentativas tenham sido feitas na superresolução cega para restaurar imagens de baixa resolução com degradações complexas e desconhecidas, elas ainda estão longe de abordar imagens degradadas do mundo real em geral,Neste trabalho, propomos a utiçização GFP-GAN que aproveita antecedentes ricos e diversos encapsulados em um GAN de face pré-treinado para restauração de face cega. Este Generative Facial Prior (GFP) é incorporado ao processo de restauração
facial por meio de camadas de transformação de recursos espaciais, o que permite que nosso método alcance um bom equilíbrio entre
realidade e fidelidade.  
## Introdução
A tarefa altamente desafiadora de estimar uma imagem de alta resolução (HR) a partir de sua contraparte de baixa resolução (LR) é conhecida como super-resolução (SR).Quando tiramos uma foto com nossos celulares, as fotos podem ter várias degradações ou ruidos, como por exemplo desfoque da câmera, ruído do sensor, artefatos de nitidez e compactação JPEG, edições e carregamento em  mídias sociais, o que gera mais compressão e ruídos que são imprevisíveis. A  restauração cega de imagens é restaurar uma imagem degradada sem usar informação da imagem real ou da função de degradação, No entanto, entradas de qualidade muito baixa podem dificultar esse processo.

## Objetivo
Neste estudo, aproveitamos Prioridade facial generativa (GFP) para restauração de rosto cego no mundo real, que consiste em gerar uma imagem de alta resolução (HR) a partir de sua contraparte de baixa resolução (LR), ou seja, dada uma imagem X que sofre uma degradação desconhecida, o objetivo é estimar uma imagem de alta qualidade ŷ, que é o mais semelhante possível à imagem da verdade fundamental y, em termos de realidade e fidelidade.
## Metodologia
O GFP-GAN é composto por um módulo de remoção de degradação (UNet) e um GAN de face pré-treinado (Style-GAN2 ), Eles são interligados por um mapeamento de código latente e várias camadas Channel-Split Spatial Feature Transform (CS-SFT).Especificamente, o módulo de remoção de degradação é projetado para remover degradação complicada e extrair dois tipos de recursos:
1. Características latentes
2. Recursos espaciais de multi-resolução
As características latentes são usadas para mapear a imagem de entrada para o código latente mais próximo no StyleGAN2  as  características espaciais  são usados para modular os recursos do StyleGAN2.
O objetivo de aprendizagem de treinar o GFP-GAN consiste em: 
1.Perda de reconstrução que restringe os resultados ŷ perto da verdade fundamental y.
2.Perda adversária para restaurar texturas realistas
3.Perda de componente facial proposta para melhorar ainda mais os detalhes faciais.
4.Perda de preservação de identidade.

