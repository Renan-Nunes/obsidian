 # Algoritmos

## 1. O que é um algoritmo?

Um **algoritmo** é uma sequência **finita, ordenada e não ambígua de instruções** utilizada para solucionar um problema ou realizar uma determinada tarefa.

Simplificando, um algoritmo descreve **como chegar a um resultado a partir de determinadas informações de entrada**.

> **Algoritmo ≠ programa.**
>
> Um algoritmo representa a parte lógica da solução. Um programa é a implementação dessa lógica utilizando uma linguagem de programação.

Por exemplo, conseguimos tornar a produção de um bolo em um algoritmo:
1. Separar os ingredientes. 
2. Misturar os ingredientes em um recipiente. 
3. Preparar a forma. 
4. Despejar a massa na forma. 
5. Pré-aquecer o forno. 
6. Colocar a forma no forno. 
7. Aguardar o tempo necessário para assar. 
8. Retirar o bolo do forno. 
9. Deixar o bolo esfriar. 
10. Servir o bolo.

---

# 2. Para que servem os algoritmos?

Algoritmos são utilizados para **organizar e estruturar a resolução de problemas**.

Antes de escrever código, é necessário compreender:

- Qual é o problema?
- Quais informações são necessárias?
- Quais operações precisam ser realizadas?
- Quais decisões precisam ser tomadas?
- Quais situações podem ocorrer?
- Qual deve ser o resultado?

O algoritmo funciona como uma **ponte entre o problema e sua implementação**.
 

---

# 3. Algoritmos na programação

### Problema

Determinar se uma pessoa é maior de idade.

### Algoritmo

1. Receber a idade.
2. Verificar se a idade é maior ou igual a 18.
3. Se for, informar que a pessoa é maior de idade.
4. Caso contrário, informar que é menor de idade.

O código é apenas uma **forma de representar e executar o algoritmo**.

O mesmo algoritmo poderia ser implementado em:

- C
- C++
- Java
- Python
- JavaScript
- C#
- entre outras linguagens.

A lógica fundamental continua sendo a mesma.

---

# 4. Como um algoritmo é construído?

A construção de um algoritmo normalmente começa com a **compreensão do problema**.

Podemos dividir esse processo em etapas:

```text
1. Compreender o problema
          ↓
2. Identificar entradas e saídas
          ↓
3. Definir as operações necessárias
          ↓
4. Organizar a sequência de execução
          ↓
5. Identificar decisões
          ↓
6. Identificar repetições
          ↓
7. Escrever o algoritmo
          ↓
8. Testar a solução
          ↓
9. Implementar em uma linguagem
```

---

# 5. Entrada, processamento e saída


---

# 6. Abstração

A construção de algoritmos envolve **abstração**.

Abstrair significa concentrar-se nos aspectos relevantes do problema e ignorar detalhes que não são necessários naquele momento.

Por exemplo, para calcular uma média:

```text
média_simples = (nota1 + nota2 + nota3) / 3
```


---

# 7. Decomposição de problemas

Problemas complexos podem ser divididos em problemas menores.

Essa técnica é chamada de **decomposição**.

Por exemplo:

> Criar um sistema de vendas.

Esse problema pode ser dividido em:

```text
Sistema de vendas
│
├── Cadastro de produtos
│
├── Cadastro de clientes
│
├── Registro de vendas
│
├── Cálculo do total
│
├── Controle de estoque
│
└── Geração de relatórios
```

A decomposição facilita:

- entendimento;
- desenvolvimento;
- testes;
- manutenção;
- identificação de erros;
- reutilização de soluções.

---

# 8. Estruturas fundamentais de um algoritmo

 
```text
SEQUÊNCIA
CONDIÇÃO
REPETIÇÃO
```

Essas estruturas também aparecem diretamente na programação.

---

## 9.1. Sequência

As instruções são executadas na ordem em que foram definidas.

```text
1. Ler número A
2. Ler número B
3. Somar A e B
4. Mostrar resultado
```


---

## 9.2. Condição

Permite que o algoritmo escolha um caminho dependendo de uma condição.
 
```text
SE idade >= 18
    informar "Maior de idade"
SENÃO
    informar "Menor de idade"
```


---

## 9.3. Repetição

Permite executar determinadas instruções várias vezes.

```text
Enquanto contador <= 10
    mostrar contador
    incrementar contador
```


---

# 10. Representação de algoritmos

Um algoritmo pode ser representado de diferentes maneiras.

## Linguagem natural

Utiliza a linguagem humana para descrever os passos.

```text
1. Ler dois números.
2. Somar os números.
3. Mostrar o resultado.
```
 

---

## Pseudocódigo

Utiliza uma linguagem estruturada, mas independente de uma linguagem de programação específica.

Exemplo:

```text
ALGORITMO Soma

    INICIO

        LEIA A
        LEIA B

        SOMA ← A + B

        ESCREVA SOMA

    FIM
```

O pseudocódigo permite concentrar-se na lógica sem precisar lidar imediatamente com a sintaxe de uma linguagem.

---

## Fluxograma

Utiliza símbolos gráficos para representar o fluxo de execução de um algoritmo.

Exemplo conceitual:

```text
       INÍCIO
          ↓
     Ler idade
          ↓
    idade >= 18?
      ↙       ↘
    SIM        NÃO
     ↓          ↓
 "Maior"     "Menor"
      ↘        ↙
         FIM
```

O fluxograma é especialmente útil para visualizar:

- sequência;
- decisões;
- repetições;
- caminhos possíveis;
- fluxo de execução.

---

# 11. Algoritmo não é necessariamente código

Um algoritmo pode existir sem um computador.

Uma receita culinária, por exemplo, possui características semelhantes às de um algoritmo:

```text
1. Separar os ingredientes.
2. Aquecer a panela.
3. Adicionar o óleo.
4. Adicionar os ingredientes.
5. Cozinhar durante determinado período.
6. Servir.
```

Entretanto, algoritmos computacionais normalmente precisam ser descritos de forma suficientemente precisa para que possam ser executados por um computador.

A diferença fundamental está no **nível de formalização e no objetivo**.

---

# 12. Algoritmos e linguagens de programação

Uma linguagem de programação fornece uma forma formal de expressar algoritmos para que um computador possa executá-los.

Podemos pensar na relação da seguinte maneira:

```text
Problema
   ↓
Solução
   ↓
Algoritmo
   ↓
Linguagem de programação
   ↓
Código-fonte
   ↓
Compilação / interpretação
   ↓
Execução
   ↓
Resultado
```

Por exemplo:

```text
Problema:
Calcular a média de três notas.

        ↓

Algoritmo:
Somar as três notas e dividir por três.

        ↓

Implementação:
C

        ↓

Código:

media = (nota1 + nota2 + nota3) / 3;
```

---

# 13. Testando um algoritmo

Um algoritmo não deve ser considerado correto apenas porque parece funcionar.

É necessário testá-lo com diferentes entradas.

Por exemplo, para um algoritmo que determina se um número é positivo, negativo ou zero:

| Entrada | Resultado esperado |
|---:|---|
| `10` | Positivo |
| `-5` | Negativo |
| `0` | Zero |

Esses casos permitem verificar diferentes caminhos da solução.

Também é importante testar **casos extremos** e situações inesperadas.


---

# 14. Eficiência de algoritmos

Além de funcionar corretamente, um algoritmo pode ser analisado quanto à sua **eficiência**.

Entre os recursos importantes estão:

- tempo de execução;
- quantidade de memória utilizada;
- número de operações realizadas;
- quantidade de dados processados.

Por exemplo, imagine que precisamos procurar um nome em uma lista.

Uma solução pode verificar os elementos um por um:

```text
João
Maria
Pedro
Carlos
Renan
...
```

Outra solução pode utilizar uma estrutura de dados que permita realizar a pesquisa de maneira mais eficiente.

Por isso, em problemas maiores, não basta perguntar:

> "Funciona?"

Também devemos perguntar:

> "Funciona corretamente e com quais custos?"

---

# 15. Algoritmos como base da programação

Programar não consiste apenas em conhecer a sintaxe de uma linguagem.

É necessário saber:

- interpretar problemas;
- identificar dados;
- definir operações;
- tomar decisões;
- controlar repetições;
- organizar informações;
- decompor problemas;
- construir soluções;
- testar resultados.

A linguagem de programação é uma ferramenta utilizada para **expressar essas soluções de maneira executável**.

---

# 17. Resumo

Um algoritmo é uma **sequência estruturada de instruções destinada à resolução de um problema ou execução de uma tarefa**.

Sua construção envolve:

```text
COMPREENDER O PROBLEMA
        ↓
IDENTIFICAR ENTRADAS E SAÍDAS
        ↓
DEFINIR O PROCESSAMENTO
        ↓
DEFINIR DECISÕES E REPETIÇÕES
        ↓
ORGANIZAR A SOLUÇÃO
        ↓
ESCREVER O ALGORITMO
        ↓
TESTAR
        ↓
IMPLEMENTAR
```

As três estruturas fundamentais são:

```text
┌─────────────────────────┐
│       ALGORITMO         │
├─────────────────────────┤
│                         │
│  SEQUÊNCIA              │
│  ↓                      │
│  execução ordenada      │
│                         │
│  CONDIÇÃO               │
│  ↓                      │
│  tomada de decisão      │
│                         │
│  REPETIÇÃO              │
│  ↓                      │
│  execução múltipla      │
│                         │
└─────────────────────────┘
```

Essas estruturas formam a base para a construção de programas em C e em praticamente todas as linguagens de programação.