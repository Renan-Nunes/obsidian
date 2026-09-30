```

## Normalização de dados

A **normalização** é um processo utilizado para **organizar os dados de um banco de dados**, buscando reduzir problemas relacionados à repetição e à inconsistência das informações.

A ideia principal é:

> **Organizar os dados de forma que cada informação fique armazenada no lugar adequado.**

---

## Por que normalizar?

Imagine uma tabela de vendas:

```text
| Pedido | Cliente | Telefone      | Produto | Preço |
|--------|---------|---------------|---------|-------|
| 1      | Renan   | 6299999-1111  | Mouse   | 100   |
| 2      | Renan   | 6299999-1111  | Teclado | 200   |
| 3      | Maria   | 6298888-2222  | Mouse   | 100   |
````

Podemos perceber que algumas informações estão sendo **repetidas**.

O telefone do Renan, por exemplo, aparece novamente sempre que ele realiza uma nova compra.

Isso pode gerar problemas.

---

## Problema da repetição

Imagine que o telefone do Renan seja alterado.

Precisaríamos alterar:

```
Pedido 1 → telefone
Pedido 2 → telefone
Pedido 3 → telefone
...
```

Se alguma ocorrência não for atualizada, teremos informações diferentes para o mesmo cliente.

```
Renan → 6299999-1111
Renan → 6298888-7777
```

O banco passa a possuir uma **inconsistência**.

A normalização busca evitar esse tipo de situação.

---

# Objetivos da normalização

De maneira geral, a normalização busca:

- reduzir a redundância de dados;
- evitar inconsistências;
- organizar melhor as informações;
- facilitar a manutenção dos dados;
- melhorar a estrutura das tabelas.

Podemos visualizar:

```
DADOS DESORGANIZADOS
        ↓
    REPETIÇÕES
        ↓
 INCONSISTÊNCIAS
        ↓
   DIFICULDADE DE
    MANUTENÇÃO
```

Com a normalização:

```
DADOS
  ↓
ORGANIZAÇÃO
  ↓
MENOS REDUNDÂNCIA
  ↓
MAIOR CONSISTÊNCIA
```

---

# Um exemplo simples

Em vez de armazenar todas as informações juntas:

```
PEDIDO
│
├── cliente
├── telefone
├── produto
├── preço
└── ...
```

Podemos separar informações que pertencem a conceitos diferentes:

```
CLIENTE
│
├── id
├── nome
└── telefone


PRODUTO
│
├── id
├── nome
└── preço


PEDIDO
│
├── id
└── cliente
```

Agora cada informação possui um **contexto mais adequado**.

O telefone pertence ao cliente.

O preço pertence ao produto.

As informações do pedido pertencem ao pedido.

---

# Normalização e organização

A normalização está diretamente relacionada à ideia de **organizar os dados de acordo com aquilo que eles representam**.

Por exemplo:

```
CLIENTE
    ↓
informações sobre clientes

PRODUTO
    ↓
informações sobre produtos

PEDIDO
    ↓
informações sobre pedidos
```

Em vez de concentrar informações diferentes em uma única estrutura, buscamos separá-las de maneira lógica.

---

# Formas normais

A normalização é organizada através de diferentes **formas normais**.

As mais conhecidas são:

```
1ª Forma Normal (1FN)
        ↓
2ª Forma Normal (2FN)
        ↓
3ª Forma Normal (3FN)
```

Cada forma normal estabelece determinadas regras para a organização dos dados.

Neste primeiro momento, o mais importante é compreender a ideia geral:

> **As formas normais são etapas utilizadas para avaliar e melhorar a organização dos dados.**

---

# A ideia da normalização

Podemos resumir o processo da seguinte maneira:

```
              NORMALIZAÇÃO
                    │
                    ↓
             ANALISAR OS DADOS
                    │
                    ↓
          IDENTIFICAR REPETIÇÕES
                    │
                    ↓
           ORGANIZAR INFORMAÇÕES
                    │
                    ↓
          REDUZIR REDUNDÂNCIAS
                    │
                    ↓
          EVITAR INCONSISTÊNCIAS
```

---

# Normalização na modelagem

A normalização faz parte do processo de modelagem de dados.

Podemos visualizar uma sequência simplificada:

```
REQUISITOS
    ↓
MODELAGEM
    ↓
MER
    ↓
MODELO RELACIONAL
    ↓
NORMALIZAÇÃO
    ↓
ESTRUTURA ORGANIZADA
    ↓
IMPLEMENTAÇÃO DO BANCO
```

O objetivo não é simplesmente **criar mais tabelas**.

A ideia é encontrar uma estrutura que represente os dados de maneira organizada, evitando repetições desnecessárias e problemas de consistência.

---

# Resumo

A **normalização** é um processo de organização dos dados que busca principalmente:

```
┌────────────────────────────┐
│       NORMALIZAÇÃO         │
├────────────────────────────┤
│                            │
│ Reduzir redundância        │
│                            │
│ Evitar inconsistências     │
│                            │
│ Organizar os dados         │
│                            │
│ Facilitar manutenção       │
│                            │
└────────────────────────────┘
```

A partir desse conceito, podemos estudar as **formas normais**, começando pela **1ª Forma Normal (1FN)**.

```

Eu seguiria exatamente essa linha para sua playlist: **conceito → problema que a normali
```