## **1. Concepção**

O projeto **Looker** foi desenvolvido por **Renan Nunes, Affonso Helmuth e Pedro Castilho**.

A proposta inicial partiu da ideia de uma **locadora**, mas o grupo optou por não seguir de um modelo **monolítico** e desmembra-lo. Em vez disso, adotou uma abordagem baseada em desenvolver do zero um **microserviços (Microservices Architecture)**, com foco acadêmico no estudo de **arquitetura limpa (Architecture Patterns)** e (**design patterns**).

Para estruturar as APIs, utilizamos também o padrão arquitetural **MVC (Model-View-Controller)**.

O sistema foi dividido em cinco principais módulos: **Usuário, Catálogo, Aluguéis, Pagamento e Auth**. A partir dessa divisão, foram implementadas as seguintes APIs:

- **API - USER**  
    Responsável pelo **CRUD de usuários** e pelo **relacionamento com os demais serviços**.  
    Desenvolvida em **Python (FastAPI)**, utilizando um banco de dados **PostgreSQL** compartilhado.
    
- **API - CATÁLOGO**  
    Responsável pelo **CRUD de filmes**.  
    Depende da **API USER** para validar permissões, permitindo que apenas usuários com o papel **ADMIN** realizem operações de inserção.  
    Desenvolvida em **Python (FastAPI)**, utilizando um banco de dados **PostgreSQL** compartilhado.
    
- **API - ALUGUEL**  
    Responsável pela lógica de **empréstimo e devolução de filmes** do catálogo.  
    Realiza operações como: quantidade de cópias, disponibilidade, controle de preço e registro de transações.  
    Para confirmar uma transação de aluguel, integra-se à **API de Pagamento (Mock)**.  
    Desenvolvida em **Python (FastAPI)**, utilizando um banco de dados **PostgreSQL** compartilhado.
    
- **API - PAGAMENTO (Mock)**  
    Responsável pela simulação de transações financeiras relacionadas aos aluguéis.  
    Atua apenas como um **mock service**, retornando respostas simuladas de aprovação, recusa ou erro.  
    Desenvolvida em **Python (FastAPI)**, sem persistência em banco de dados (respostas em memória).
    
- **API - AUTH**  
    Responsável pela **autenticação de usuários** e pela definição de **claims (SignedAt, SignedUser),** ela é feita em si em cima do USER através de um JWT.  
    Atua como **camada de segurança** acima das demais APIs, sendo acessada via API Gateway.  
    Desenvolvida em **Java (Spring Boot)**.
    

A comunicação entre as APIs ocorre exclusivamente por meio de um **API Gateway (Spring Cloud Gateway)**, que atua como **orquestrador**. Ele recebe as requisições dos usuários, direciona ao microserviço adequado e retorna as respostas.

---

## **2. Padrões Utilizados**

Além do padrão **MVC**, foram aplicados os seguintes padrões de arquitetura e design patterns:

- **DTO (Data Transfer Object):** utilizado para transferência de dados entre endpoints e schemas, permitindo validações mínimas e aplicação de regras de negócio.
    
- **Factory:** utilizado para padronizar a criação de entidades persistidas no banco de dados.
    
- **Publish-Subscriber (Observer Pattern):** implementado por meio de **Angular Observables** e **EventEmitter**, permitindo comunicação reativa entre componentes.
    

---

## **3. Versionamento**

O versionamento foi realizado com **Git & GitHub**, utilizando o fluxo de trabalho baseado no **Gitflow**.  
As branches foram criadas seguindo o padrão `feat/<nome-da-branch>`.
Ambos os micro-services estão sendo mergeados em pastas isoladas na main para melhorar a organização.

Além disso, foi utilizado o **Alembic** para gerenciamento e execução das **migrations** do banco de dados.

---

## **4. Testes de Rotas e Documentação de Endpoints**

A documentação de cada API foi gerada automaticamente via **Swagger**, integrado ao FastAPI e ao Spring Boot.  
Isso permitiu a **visualização e execução de testes de endpoints** diretamente pela interface interativa.

Rotas disponíveis:

- **USER API** → [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
    
- **ALUGUÉIS API** → [http://127.0.0.1:8001/docs](http://127.0.0.1:8001/docs)
    
- **CATÁLOGO API** → [http://127.0.0.1:8002/docs](http://127.0.0.1:8002/docs)
    
- **PAGAMENTO API (Mock)** → [http://127.0.0.1:8004/docs](http://127.0.0.1:8004/docs)
    
- **AUTH API** → [http://127.0.0.1:8003/docs](http://127.0.0.1:8003/docs)
    

A unificação das documentações individuais foi realizada por meio do **SwaggerUIBundle**, permitindo centralização e consulta em um único ponto.

![[Pasted image 20250822203727.png]]
![[Pasted image 20250822203917.png]]