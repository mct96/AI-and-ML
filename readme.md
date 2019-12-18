# Algoritmo Genético

Implementação do algoritmo genético para a solução do problema do caxeiro viajante. A implementação desse algoritmo possui algumas variações em relação a forma canônica.

### Heurística Implementada

Diferente de muitas implementações que utiliza os cromossomos no intervalo [0, 1], está implementação utiliza o nome da cidade como cromossomo. Nos teste realizados há 15 cidades, ou seja, 15 possibilidades para cada cromossomo. Para otimizar o processo (acelerar a convergência) a escolha de qual cidade substituir no caso de mutação é feita por meio de um heurística. Essa heuristica seleciona a cidade que reduz o custo da função de *fitness*.

### Parâmetros

Esta implementação possui diversos parâmetros para ajuste. Entre eles:
- Tamanho da população
- Tamanho do genes
- Função de *fitness*
- Número máximo de gerações
- Probabilidade de mutação.

### Algumas considerações
- A convergência não é garantida, porém não estou certo se isso se deve a implementação ou a natureza do problema de teste.
- A escolha dos indivíduos selecionados para o **crossover** é feita iterativamente formando pares baseado no valor de fitness associado a cada indivíduo. Ex: Ind_1 com Ind_2, Ind_3 com Ind_4, e assim por diante.
- Seleção da porção para o crossover é feito através da escolha de uma porção qualquer do genes, em vez de usar a porção inicial.

### Demonstrações

![Amostra 1](/resources/amostra_1.gif)
![Amostra 2](/resources/amostra_2.gif)
![Amostra 3](/resources/amostra_3.gif)

Exemplo de execução:

> Legenda:
|Simbolo|Significado|
|-|-|
|[...]|Geração|
|hg|Maior valor da geração|
|av|Valor médio da geração|
|prob|Probabilidade de haver mutação|
```bash
[0    ] hg: -35100.00, av: -16746.00, prob: 0.30
[10   ] hg: -3600.00, av: -17264.00, prob: 0.30
[20   ] hg: -3600.00, av: -11374.00, prob: 0.30
[30   ] hg: -2800.00, av: -9382.00, prob: 0.30
[40   ] hg: -2800.00, av: -8238.00, prob: 0.30
[50   ] hg: -1800.00, av: -8322.00, prob: 0.30
[60   ] hg: -1800.00, av: -7652.00, prob: 0.30
[70   ] hg: -1800.00, av: -7292.00, prob: 0.30
[80   ] hg: -1800.00, av: -7182.00, prob: 0.30
[90   ] hg: -1800.00, av: -6656.00, prob: 0.30
[100  ] hg: -1800.00, av: -7388.00, prob: 0.30
[110  ] hg: -1800.00, av: -6852.00, prob: 0.30
[120  ] hg: -1800.00, av: -7056.00, prob: 0.30
[130  ] hg: -1800.00, av: -6528.00, prob: 0.30
[140  ] hg: -1600.00, av: -6404.00, prob: 0.30
[150  ] hg: -1600.00, av: -6416.00, prob: 0.30
[160  ] hg: -1600.00, av: -6862.00, prob: 0.30
[170  ] hg: -1600.00, av: -6448.00, prob: 0.30
[180  ] hg: -1600.00, av: -6780.00, prob: 0.30
[190  ] hg: -1600.00, av: -6678.00, prob: 0.30
[200  ] hg: -1600.00, av: -6404.00, prob: 0.30
[210  ] hg: -1600.00, av: -6524.00, prob: 0.30
[220  ] hg: -1600.00, av: -5978.00, prob: 0.30
[230  ] hg: -1600.00, av: -6118.00, prob: 0.30
[240  ] hg: -1600.00, av: -6186.00, prob: 0.30
[250  ] hg: -1600.00, av: -6312.00, prob: 0.30
[260  ] hg: -1600.00, av: -6098.00, prob: 0.30
[270  ] hg: -1600.00, av: -6408.00, prob: 0.30
[280  ] hg: -1500.00, av: -6148.00, prob: 0.30
[290  ] hg: -1500.00, av: -6364.00, prob: 0.30
[300  ] hg: -1500.00, av: -6728.00, prob: 0.30
[310  ] hg: -1500.00, av: -5968.00, prob: 0.30
[320  ] hg: -1300.00, av: -6020.00, prob: 0.30
[330  ] hg: -1300.00, av: -6800.00, prob: 0.30
[340  ] hg: -1300.00, av: -6010.00, prob: 0.30
[350  ] hg: -1300.00, av: -5870.00, prob: 0.30
[360  ] hg: -1300.00, av: -6560.00, prob: 0.30
[370  ] hg: -1200.00, av: -5720.00, prob: 0.30
[380  ] hg: -1200.00, av: -5686.00, prob: 0.30
[390  ] hg: -1200.00, av: -6138.00, prob: 0.30
[400  ] hg: -1200.00, av: -6458.00, prob: 0.30
[410  ] hg: -1200.00, av: -5972.00, prob: 0.30
[420  ] hg: -1200.00, av: -5976.00, prob: 0.30
[430  ] hg: -1200.00, av: -5526.00, prob: 0.30
[440  ] hg: -1200.00, av: -5582.00, prob: 0.30
[450  ] hg: -1200.00, av: -5316.00, prob: 0.30
[460  ] hg: -1200.00, av: -5998.00, prob: 0.30
[470  ] hg: -1200.00, av: -5792.00, prob: 0.30
[480  ] hg: -1200.00, av: -5698.00, prob: 0.30
[490  ] hg: -1200.00, av: -5878.00, prob: 0.30
[500  ] hg: -1200.00, av: -6040.00, prob: 0.30
[510  ] hg: -1200.00, av: -6002.00, prob: 0.30
[520  ] hg: -1200.00, av: -5400.00, prob: 0.30
[530  ] hg: -1200.00, av: -5682.00, prob: 0.30
[540  ] hg: -1200.00, av: -6268.00, prob: 0.30
[550  ] hg: -1200.00, av: -5912.00, prob: 0.30
[560  ] hg: -1000.00, av: -5788.00, prob: 0.30
[570  ] hg: -1000.00, av: -4708.00, prob: 0.30
[580  ] hg: -1000.00, av: -5814.00, prob: 0.30
[590  ] hg: -1000.00, av: -5742.00, prob: 0.30
[600  ] hg: -1000.00, av: -5812.00, prob: 0.30
[610  ] hg: -1000.00, av: -5810.00, prob: 0.30
[620  ] hg: -1000.00, av: -5006.00, prob: 0.30
[630  ] hg: -1000.00, av: -5436.00, prob: 0.30
[640  ] hg: -1000.00, av: -5358.00, prob: 0.30
[650  ] hg: -1000.00, av: -5742.00, prob: 0.30
[660  ] hg: -800.00, av: -6214.00, prob: 0.30
[670  ] hg: -800.00, av: -6048.00, prob: 0.30
[680  ] hg: -800.00, av: -5410.00, prob: 0.30
[690  ] hg: -800.00, av: -4846.00, prob: 0.30
[700  ] hg: -800.00, av: -5454.00, prob: 0.30
[710  ] hg: -800.00, av: -5354.00, prob: 0.30
[720  ] hg: -800.00, av: -4824.00, prob: 0.30
[730  ] hg: -800.00, av: -5382.00, prob: 0.30
[740  ] hg: -800.00, av: -5632.00, prob: 0.30
[750  ] hg: -800.00, av: -5616.00, prob: 0.30
[760  ] hg: -800.00, av: -5782.00, prob: 0.30
[770  ] hg: -800.00, av: -5458.00, prob: 0.30
[780  ] hg: -800.00, av: -5448.00, prob: 0.30
[790  ] hg: -800.00, av: -5504.00, prob: 0.30
[800  ] hg: -800.00, av: -5454.00, prob: 0.30
[810  ] hg: -800.00, av: -5508.00, prob: 0.30
[820  ] hg: -600.00, av: -5510.00, prob: 0.30
[830  ] hg: -600.00, av: -5408.00, prob: 0.30
[840  ] hg: -600.00, av: -5192.00, prob: 0.30
[850  ] hg: -600.00, av: -4990.00, prob: 0.30
[860  ] hg: -600.00, av: -5006.00, prob: 0.30
[870  ] hg: -600.00, av: -5196.00, prob: 0.30
[880  ] hg: -600.00, av: -4456.00, prob: 0.30
[890  ] hg: -600.00, av: -5132.00, prob: 0.30
[900  ] hg: -600.00, av: -4872.00, prob: 0.30
[910  ] hg: -600.00, av: -4796.00, prob: 0.30
[920  ] hg: -600.00, av: -5786.00, prob: 0.30
[930  ] hg: -600.00, av: -5380.00, prob: 0.30
[940  ] hg: -600.00, av: -4700.00, prob: 0.30
[950  ] hg: -600.00, av: -4458.00, prob: 0.30
[960  ] hg: -600.00, av: -5264.00, prob: 0.30
[970  ] hg: -400.00, av: -5292.00, prob: 0.30
[980  ] hg: -400.00, av: -4486.00, prob: 0.30
[990  ] hg: -400.00, av: -5110.00, prob: 0.30
[1000 ] hg: -400.00, av: -4856.00, prob: 0.30
[1010 ] hg: -400.00, av: -4890.00, prob: 0.30
[1020 ] hg: -400.00, av: -5620.00, prob: 0.30
[1030 ] hg: -400.00, av: -4506.00, prob: 0.30
[1040 ] hg: -400.00, av: -4930.00, prob: 0.30
[1050 ] hg: -400.00, av: -4954.00, prob: 0.30
[1060 ] hg: -400.00, av: -5750.00, prob: 0.30
[1070 ] hg: -400.00, av: -4844.00, prob: 0.30
[1080 ] hg: -200.00, av: -4650.00, prob: 0.30
[1090 ] hg: -200.00, av: -4894.00, prob: 0.30
[1100 ] hg: -200.00, av: -4700.00, prob: 0.30
[1110 ] hg: -200.00, av: -4708.00, prob: 0.30
[1120 ] hg: -200.00, av: -4010.00, prob: 0.30
[1130 ] hg: -200.00, av: -4954.00, prob: 0.30
[1140 ] hg: -200.00, av: -4350.00, prob: 0.30
[1150 ] hg: -200.00, av: -3626.00, prob: 0.30
Highest value reached.
['B', 'N', 'M', 'F', 'K', 'O', 'I', 'G', 'G', 'E', 'L', 'D', 'C', 'J', 'A'] -> f: -15700.000000 d:7100.000000
['O', 'F', 'N', 'D', 'K', 'J', 'I', 'H', 'H', 'E', 'L', 'M', 'B', 'C', 'A'] -> f: -14800.000000 d:6200.000000
['F', 'N', 'M', 'L', 'B', 'H', 'H', 'O', 'G', 'E', 'I', 'D', 'C', 'K', 'J'] -> f: -14800.000000 d:6200.000000
['N', 'D', 'C', 'L', 'O', 'L', 'I', 'B', 'F', 'H', 'E', 'K', 'J', 'G', 'A'] -> f: -14700.000000 d:6100.000000
['O', 'M', 'K', 'L', 'D', 'J', 'H', 'H', 'G', 'E', 'A', 'N', 'C', 'B', 'I'] -> f: -14600.000000 d:6000.000000
['O', 'L', 'N', 'K', 'K', 'M', 'I', 'F', 'G', 'E', 'B', 'J', 'C', 'H', 'A'] -> f: -13600.000000 d:5000.000000
['O', 'A', 'D', 'L', 'K', 'J', 'I', 'M', 'G', 'E', 'F', 'H', 'C', 'C', 'B'] -> f: -13500.000000 d:4900.000000
['I', 'N', 'L', 'M', 'K', 'J', 'O', 'D', 'G', 'E', 'F', 'C', 'C', 'H', 'A'] -> f: -13400.000000 d:4800.000000
['O', 'N', 'H', 'L', 'K', 'J', 'I', 'G', 'G', 'E', 'F', 'D', 'C', 'M', 'A'] -> f: -13000.000000 d:4400.000000
['O', 'N', 'M', 'E', 'J', 'K', 'I', 'H', 'G', 'D', 'F', 'C', 'C', 'B', 'A'] -> f: -11600.000000 d:3000.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'B', 'F', 'D', 'C', 'C', 'A'] -> f: -10800.000000 d:2200.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'G', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -10200.000000 d:1600.000000
['N', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -10100.000000 d:1500.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'E', 'D', 'C', 'B', 'A'] -> f: -10000.000000 d:1400.000000
['O', 'M', 'L', 'J', 'K', 'C', 'I', 'F', 'G', 'E', 'H', 'D', 'A', 'B', 'N'] -> f: -3500.000000 d:4900.000000
['O', 'N', 'M', 'L', 'I', 'J', 'D', 'H', 'G', 'C', 'F', 'B', 'E', 'K', 'A'] -> f: -3400.000000 d:4800.000000
['O', 'N', 'M', 'L', 'K', 'J', 'E', 'H', 'D', 'G', 'F', 'I', 'C', 'B', 'A'] -> f: -1800.000000 d:3200.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'E', 'F', 'D', 'C', 'B', 'A'] -> f: -200.000000 d:1600.000000
['O', 'N', 'M', 'L', 'K', 'J', 'I', 'H', 'G', 'F', 'E', 'D', 'C', 'B', 'A'] -> f: 0.000000 d:1400.000000
```
