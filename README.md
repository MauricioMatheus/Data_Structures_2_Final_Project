# Grafos e Estruturas Complexas  

# Parte 1



## Autores: 
### • Lucas Garcia Costa   

### • Maurício Matheus Araújo Silva Galvão    

Link do vídeo explicativo: https://youtu.be/dUB-AmqJT9U

Neste projeto, além das bibliotecas do Python `Networkx`, `Matplotlib`, `Pandas` e `Numpy` também foi utilizado o Gephi para auxílio das análises de redes complexas.   

### Requisito 1: Centralidades e Dimensionamento de vértices    

Primeiramente foi feita a distribuição dos nós para melhor visualização com utilização do ForceAtlas2, para assim dimensionarmos os vértices de acordo com as suas quantidades de vizinhos. As cores foram relacionadas a Eigenvector, Closeness e Betweenness Centrality:  

### Eigenvector Centrality (Azul → Vermelho):  

![image](https://github.com/user-attachments/assets/49e5f22a-10d3-4c26-bb85-ebdd86615fe5)     

Podemos observar que a influência na proteína não é distribuída de forma igual. Ela está altamente concentrada em um pequeno grupo de nós na parte inferior.  

![eigenvector-centralities](https://github.com/user-attachments/assets/f34f2110-2153-4c2e-8bc5-ed383f830af4)  

Este gráfico confirma visualmente o que a Centralidade de Autovetor representa: a influência na rede não é distribuída de forma igual.  


### Closeness Centrality (Azul → Vermelho):  

![image](https://github.com/user-attachments/assets/f424433f-c5df-4e12-b235-35898d6da319)   

A maioria dos nós estão em (azul/verde). Isso significa que a maior parte da estrutura da proteína é composta por resíduos que estão, em média, distantes de todos os outros.  

![Closeness Centrality Distribution](https://github.com/user-attachments/assets/6c5b54b2-5c5b-497a-af8f-f2c55b1adcaa)  

A maioria dos nós são periféricos. O gráfico de distribuição confirma que a grande maioria dos nós (resíduos) possui uma baixa pontuação de proximidade, com valores concentrados perto de zero.  

### Betweenness Centrality (Azul → Vermelho):  

![image](https://github.com/user-attachments/assets/b49f05b4-6933-4fd7-8d47-5bf5e7966a84)  

A rede da proteína possui pontos de controle e vulnerabilidade bem definidos.    

![Betweenness Centrality Distribution](https://github.com/user-attachments/assets/675771cc-e4d1-4d4f-97da-aed153983e70)

O gráfico reforça que a esmagadora maioria dos resíduos não participa dos caminhos mais curtos entre outras partes da rede.  

### Degree Centrality (Azul → Vermelho):  

![image](https://github.com/user-attachments/assets/d8e72ca0-bde8-4f4c-b65e-a97239fa770b)  

Os nós maiores e de cor mais quente (vermelho e laranja) são os hubs da rede. Eles são os resíduos que possuem o maior número de conexões diretas e atuam como pontos centrais de ancoragem em suas vizinhanças.  

![degree-distribution](https://github.com/user-attachments/assets/ad1c309b-21c5-42cd-a958-e603801ac1ae)  

O gráfico reforça que a estrutura é mantida por um pequeno número de hubs muito importantes que concentram um grande número de interações, enquanto a vasta maioria dos nós forma apenas conexões locais.  


### Requisito 2: K-core e K-shell  

Na sequência, foram analisados o k-core e k-shell da rede.

### K-core and K-shell (Preto → Cinza → Azul → Vermelho):

![image](https://github.com/user-attachments/assets/b571a236-eae3-475f-b9c5-e171823b1136)  

A rede não é uniforme, mas organizada com camadas de densidade distintas. Ela possui um núcleo pequeno (o 3-core), um corpo estrutural principal (a 2-shell) e uma vasta periferia de nós com poucas conexões (as camadas 0 e 1), o que indica uma estrutura robusta e estável em seu centro.  

### Requisito 3: Comunidades e Modularidade  

Por fim, transformamos a rede de proteínas estática em uma visualização de web interativa e "em produção", permitindo a exploração dinâmica do grafo. Para isso, a rede foi primeiramente analisada no Gephi para detectar comunidades através do cálculo de Modularidade, onde cada comunidade (grupo de nós densamente conectados) foi representada por uma cor distinta. O tamanho dos nós foi definido pelo grau.  

Link para a visuailzação web interativa: https://steady-sundae-a3f31d.netlify.app/  

Conclui-se que a análise de comunidades e modularidade revela que a sua rede de proteínas é altamente organizada e modular.  

# Parte 2  

Na parte 2 do projeto, optamos por analisar o fator de crescimento 1GZR, fazendo um processo de estudo bastante parecido com a primeira parte.  

### Fator de crescimento 1GZR

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/0312e18f-178a-4365-adb9-e815ecabbb4f" />    

## Requisito 1: 

Foi feita a distribuição dos nós com utilização do ForceAtlas2 e posteriormente os vértices foram analisados com base em suas quantidades de vizinhos. As cores foram relacionadas a:  

### Eigenvector Centrality (Azul → Vermelho):  

<img width="714" height="816" alt="image" src="https://github.com/user-attachments/assets/5d395d32-85ce-4900-99c9-4f66f970752d" />  

<img width="600" height="400" alt="eigenvector-centralities" src="https://github.com/user-attachments/assets/92aad781-50eb-4552-9d3f-e3592f4ae1b5" />      

A influência na rede é altamente concentrada e hierárquica. A rede é dominada por um pequeno grupo de nós influentes que se reforçam mutuamente, enquanto a maioria dos outros nós atua como uma periferia com pouca ou nenhuma influência na dinâmica global.  


### Closeness Centrality (Azul → Vermelho):  

<img width="789" height="825" alt="image" src="https://github.com/user-attachments/assets/7eaeb56c-9bc1-4426-99d9-e89a21dc1b95" />  

<img width="600" height="400" alt="Closeness Centrality Distribution" src="https://github.com/user-attachments/assets/649f0fdb-857d-48b9-8f4b-acfdd6af6cfe" />  

A estrutura de núcleo-periferia é bem definida. A maioria dos nós está na periferia, enquanto um pequeno núcleo de nós é muito eficiente para alcançar toda a rede (valores altos).  

### Betweenness Centrality (Azul → Vermelho):  

<img width="786" height="776" alt="image" src="https://github.com/user-attachments/assets/b5df0e73-8657-4d32-8f6b-cbbe05ecdcb4" />  

<img width="600" height="400" alt="Betweenness Centrality Distribution" src="https://github.com/user-attachments/assets/1b2d8a79-9537-41cd-9536-f7d22a3a1a1b" />  

A função de "ponte" é altamente especializada, com a vasta maioria dos nós tendo intermediação zero. A comunicação entre diferentes regiões da rede depende de um grupo muito pequeno e exclusivo de nós críticos.  

### Degree Centrality (Azul → Vermelho):  

<img width="791" height="849" alt="image" src="https://github.com/user-attachments/assets/1b5281f2-db0e-426e-b04e-1152f752b56c" />  

<img width="600" height="400" alt="degree-distribution" src="https://github.com/user-attachments/assets/eb00a751-d0e1-435f-84b2-027be45f949e" />  

A maioria dos nós tem poucas conexões, enquanto um pequeno número de "hubs" concentra muitas interações. Isso revela uma rede heterogênea e robusta, típica de sistemas biológicos.  

## Requisito 2: K-core e K-shell  

<img width="779" height="836" alt="image" src="https://github.com/user-attachments/assets/2f7dcc8c-3098-493a-b45d-fb559b80ef11" />  

• É possível visualizar uma clara organização em camadas de densidade, com um núcleo bem definido. O grupo de nós em vermelho representa o 2-core, o núcleo mais denso e estável da rede. Este é o "coração" estrutural, fundamental para a estabilidade da molécula;   

• Os nós em ciano formam o 1-shell, a camada intermediária que constitui o corpo principal da proteína e conecta o núcleo à periferia;   

• Os nós em cinza são o 0-shell, a camada mais externa e menos conectada, representando a superfície flexível da estrutura.  

## Requisito 3:  

### Distribuição de grau (PDF)  

<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/be906f89-dbea-419d-9f14-42ddf9a526fb" />  

Pode-se observar que os graus mais comuns (mais prováveis) na rede são 0 a 2, os quais são os picos do histograma. A probabilidade diminnui rapidamente para graus mais altos.  

### Distribuição de grau (CDF)  

<img width="567" height="455" alt="image" src="https://github.com/user-attachments/assets/51ce441b-7be5-4d22-8b32-6ba27a97f782" />  

Podemos visualizar a soma das probabilidades. Ao somar as probabilidades dos nós de grau 0, 1 e 2, já se cobre aproximadamente 70% de todos os nós da rede.  

### Quartis  

<img width="155" height="91" alt="image" src="https://github.com/user-attachments/assets/fe3c5d32-88e7-4ecf-9935-bad793c8e038" />  

• Em 25% (0.25) o valor é 1.0. Significa que 25% de todos os nós da rede têm grau 1 ou menos;  

• Em 50% (0.50, Mediana) o valor é 2.0. Significa que metade de todos os nós da rede tem 2 ou menos conexões;  

• 75% (0.75): O valor é 3.0. 75% de todos os nós têm grau 3 ou menos.    

### Análise multivariável  

<img width="985" height="986" alt="image" src="https://github.com/user-attachments/assets/92e30d27-cd34-452f-bfff-3dcb0ff1dbd2" />  

• O pair plot representa fortes correlações positivas entre Degree Centrality, Closeness Centrality e Eigenvector Centrality, formando uma tendência diagonal clara, subindo da esquerda para direita. Com esses resultados podemos concluir que na nossa proteína, os nós que possuem os graus mais altos também tendem a ser os mais eficientes para espalhar informação (Alta proximidade) e os mais influentes (alto autovetor).  

• A Betweenness Centrality também se correlaciona positivamente com as outras, mas a relação é mais desorganizada (Os pontos estão espalhados). Isso revela que nem todo nó com muias conexões é necessariamente uma ponte.  

## Requisito 4:  Comunidades e Modularidade  

Por fim, transformamos a rede de proteínas em uma visualização de web interativa e "em produção", permitindo a exploração dinâmica do grafo.   

Link para a visualização web interativa:  

https://silly-khapse-c9f5b9.netlify.app/






















































