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










