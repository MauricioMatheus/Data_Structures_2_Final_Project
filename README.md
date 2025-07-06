# Grafos e Estruturas Complexas

## Autores: 
### • Lucas Garcia Costa   

### • Maurício Matheus Araújo Silva Galvão  

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














