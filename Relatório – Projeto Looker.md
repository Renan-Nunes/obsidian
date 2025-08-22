
### **1. Concepção**

O projeto **Looker** foi desenvolvido por **Renan Nunes Lima, Affonso e Pedro**.  
A proposta inicial partiu da ideia de uma **locadora online**. A partir dessa concepção, o grupo direcionou o desenvolvimento para fins acadêmicos, com foco no estudo da **arquitetura de microserviços (Micro-service)**.

Para estruturar as APIs, utilizamos também o padrão arquitetural **MVC (Model-View-Controller)**.

O sistema foi dividido em três principais módulos (ou telas): **Usuário, Aluguéis e Catálogo**. A partir disso, criamos as seguintes APIs individuais:

- **API - USER**  
    Responsável pelo CRUD de usuários.  
    Desenvolvida em **Python (FastAPI)**, com banco de dados individual em **PostgreSQL**.
    
- **API - FILM**  
    Responsável pelo catálogo de filmes e pela lógica de aluguéis.  
    Depende da **API USER** para validação das regras de negócio.  
    Desenvolvida em **Python (FastAPI)**, com banco de dados individual em **PostgreSQL**.
    
- **API - AUTH**  
    Responsável pela autenticação de usuários e definição de papéis (roles).  
    Funciona como camada de segurança acima das demais APIs.  
    Desenvolvida em **Java (Spring Boot)**.
    

A comunicação entre as APIs ocorre exclusivamente por meio de um **API Gateway (Cloudflare)**, que atua como **orquestrador**. Esse gateway recebe as requisições dos usuários, direciona para o microserviço correto e retorna a resposta.

---

### **2. Padrões Utilizados**

Além do padrão **MVC**, foram aplicados **Design Patterns** importantes no desenvolvimento:

- **DTO (Data Transfer Object):** utilizado para transferência de dados entre endpoints e schemas, permitindo validações mínimas e aplicação de regras de negócio.
    
- **Factory:** empregado para padronizar a criação das entidades que serão persistidas no banco de dados.
    

---

### **3. Versionamento**

Para o controle de versão utilizamos **Git & GitHub**, adotando o fluxo de trabalho baseado no **Gitflow**.  
As branches foram criadas com o prefixo `feat/<nome-da-feature>`.  
Além disso, utilizamos o **Alembic** para execução das **migrations** do banco de dados.

---

### **4. Documentação**

A documentação da API foi gerada automaticamente por meio do **Swagger**, integrado às bibliotecas REST utilizadas no projeto. Isso permitiu melhor visualização e teste dos endpoints.

  ![[Pasted image 20250821225137.png]]