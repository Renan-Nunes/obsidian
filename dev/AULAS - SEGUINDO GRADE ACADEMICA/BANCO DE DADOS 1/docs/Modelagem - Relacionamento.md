## MER — Modelo Entidade-Relacionamento

O **Modelo Entidade-Relacionamento (MER)** é um modelo conceitual utilizado para **representar informações de um determinado contexto e as relações existentes entre elas**.

A ideia é compreender o problema antes de pensar em como essas informações serão armazenadas em um banco de dados.

Por exemplo, imagine um sistema de uma escola.

Podemos identificar algumas informações importantes:

```text
ALUNO
PROFESSOR
DISCIPLINA
```

Mas essas informações não existem de maneira isolada.

Existe uma relação entre elas:

```text
ALUNO ─────── CURSA ─────── DISCIPLINA

PROFESSOR ─── MINISTRA ──── DISCIPLINA
```

O MER busca justamente representar **quais são os elementos envolvidos no problema e como eles se relacionam**.

---

## Entidades

As **entidades** representam os elementos que fazem parte do contexto que estamos modelando.

No exemplo de uma escola:

```text
ALUNO
PROFESSOR
DISCIPLINA
```

Podemos pensar em uma entidade como algo sobre o qual queremos representar informações dentro daquele contexto.

---

## Atributos

Os **atributos** representam características de uma entidade.

Por exemplo:

```text
ALUNO
│
├── Nome
├── Matrícula
└── Data de nascimento
```

Ou:

```text
DISCIPLINA
│
├── Nome
├── Código
└── Carga horária
```

Os atributos ajudam a **descrever as entidades**.

---

## Relacionamentos

Os **relacionamentos** representam as associações existentes entre as entidades.

Por exemplo:

```text
ALUNO ───── CURSA ───── DISCIPLINA
```

Nesse caso:

- `ALUNO` é uma entidade;
- `DISCIPLINA` é uma entidade;
- `CURSA` representa a relação entre elas.

Outro exemplo:

```text
CLIENTE ───── REALIZA ───── PEDIDO
```

O relacionamento descreve **como os elementos do sistema estão associados**.

---

## Cardinalidade

Além de identificar que existe uma relação, precisamos compreender **quantos elementos podem participar dela**.

Por exemplo:

```text
CLIENTE ───── REALIZA ───── PEDIDO
   1                         N
```

Um cliente pode realizar vários pedidos.

Outro exemplo:

```text
ALUNO ───── CURSA ───── DISCIPLINA
  N                       N
```

Um aluno pode cursar várias disciplinas e uma disciplina pode possuir vários alunos.

As principais cardinalidades que encontraremos são:

```text
1 : 1
1 : N
N : N
```

---

## Visualizando o MER

Podemos pensar no Modelo Entidade-Relacionamento como uma forma de responder:

```text
┌──────────────────────────────────────┐
│              MER                     │
│                                      │
│  O que existe?                      │
│       ↓                              │
│  ENTIDADES                           │
│                                      │
│  Como podemos descrevê-los?         │
│       ↓                              │
│  ATRIBUTOS                           │
│                                      │
│  Como estão relacionados?           │
│       ↓                              │
│  RELACIONAMENTOS                     │
│                                      │
│  Quantos podem se relacionar?       │
│       ↓                              │
│  CARDINALIDADE                       │
└──────────────────────────────────────┘
```

O objetivo do MER, portanto, é **representar conceitualmente um determinado domínio**, permitindo compreender seus elementos e as relações entre eles antes da implementação do banco de dados.

> **MER é uma representação conceitual do problema.**

A partir dele, podemos posteriormente construir modelos mais próximos da implementação do banco de dados.

---

# Exemplo simples

Imagine uma biblioteca:

```text
┌────────────┐          ┌──────────────┐
│   USUÁRIO  │          │     LIVRO    │
└────────────┘          └──────────────┘
       │                       │
       │                       │
       └─────── EMPRESTA ─────┘
```

Podemos identificar:

**Entidades:**

```text
USUÁRIO
LIVRO
```

**Relacionamento:**

```text
EMPRESTA
```

**Atributos:**

```text
USUÁRIO
├── nome
└── matrícula

LIVRO
├── título
└── autor
```

Nesse exemplo, o MER nos permite visualizar **quem participa do sistema, quais características são importantes e como essas informações se relacionam**.
