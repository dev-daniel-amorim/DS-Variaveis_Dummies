# Variáveis Dummies

São variáveis binárias representadas por 0 ou 1, indicando ausência ou presença respectivamente de atributos em variáveis categoricas. As máquinas só entendem números e não letras, por isso a necessidade de se converter variáveis do tipo texto em números que possam ser interpretados pelas máquinas.  

# Tipos de variáveis

![variaveis](https://user-images.githubusercontent.com/115194365/212817323-822179a9-966b-4092-8da0-643c96fe3b86.png)<br>

Numéricos: Como proprio nome diz, são variaveis representadas por números:
   * Discreto: Representa algo naquele momento, número de chegada, numéro da casa e etc.
   * Continuo: Valor de algo continuo, PI, massa da terra etc.

Categórico: Representádo por algo que não é numérico:
   * Nominal: sexo - masculino e feminino (não há hierarquia)
   * Ordinal: desenvolvedor - junior, pleno, senior (há hierarquia)

# Conversão de dados categóricos em váriáveis Dummies
Para converter os dados em variáveis Dummies existem alguns métodos que podemos usar e facilitar nossa vida, como:

   * Método Label Encoder
   * Método One-hot Encoder

Vamos ver cada uma delas:

### Método Label Encoder
Esse método consistem em atribuir um numero inteiro exclusivo para cada categoria com base na ordem alfabética.<br>
<a href='https://github.com/dev-daniel-amorim/DS-Variaveis_Dummies/blob/main/Label%20e%20one-hot%20encoder.ipynb'> Clique aqui para ver exemplo no código fonte. </a><br>

### Método One-hot encoder
Esse metodo separa cada categoria por coluna, criando uma matriz de 0 e 1s.<br>
<a href='https://github.com/dev-daniel-amorim/DS-Variaveis_Dummies/blob/main/Label%20e%20one-hot%20encoder.ipynb'> Clique aqui para ver exemplo no código fonte. </a><br>

### MULTICOLINEARIDADE

   * O One-Hot encode resulta em dummie variable trap, (armadilha das variáveis fictícias) onde as variáveis podem ficar altamente correlacionadas ocasionando o problema de multicolinearidade, que é quando a ligação entre elas são tão fortes que uma fica ligada diretamente a outra influenciando na nossa predição. <br>
   * Tabela de medição multicolinearidade (VIF, variance inflation factor)
        - VIF = 1 : Menos multicolinearidade
        - VIF < 5 : multicolinearidade moderada
        - VIF > 5 : multicolinearidade extrema (isso que devemos evitar)
   * Para evitar esse problema algumas das variáveis dummies deve ser descartada, para isso usaremos a função para medir o nível de pontuação VIF:<br>
<a href='https://github.com/dev-daniel-amorim/DS-Variaveis_Dummies/blob/main/Label%20e%20one-hot%20encoder.ipynb'> Clique aqui para ver a função no código fonte. </a><br>
