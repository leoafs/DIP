# Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data
## Resumo
Embora muitas tentativas tenham sido feitas na superresolução cega para restaurar imagens de baixa resolução com degradações complexas e desconhecidas, elas ainda estão longe
de abordar imagens degradadas do mundo real em geral,Neste trabalho, estendemos o método ESRGAN para uma aplicação
prática de restauração , Real-ESRGAN, que é treinada com dados sintéticos puros.  Este trabalho propõe um processo de degradação de alta ordem para modelar degradações práticas e reais, Real-ESRGAN treinado com dados puramente sintéticos é capaz de restaurar a maioria das imagens do mundo real e obter melhor desempenho visual. 
## Introdução
A tarefa altamente desafiadora de estimar uma imagem de alta resolução (HR) a partir de sua contraparte de baixa resolução (LR) é conhecida como super-resolução (SR).Quando tiramos uma foto com nossos celulares, as fotos podem ter várias degradações ou ruidos, como por exemplo desfoque da câmera, ruído do sensor, artefatos de nitidez e compactação JPEG, edições e carregamento em  mídias sociais, o que gera mais compressão e ruídos que são imprevisíveis. Super resolução cega visa restaurar imagens de baixa resolução que sofrem de degradações desconhecidas e complexas.


