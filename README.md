# GerenciamentoContatos

# Sistema de Gerenciamento de Contatos

Este é um sistema de gerenciamento de contatos para a empresa **Comércio S.A.**, desenvolvido utilizando **Java**, **Spring Boot**, **Hibernate**, **HTML**, **CSS**, **JavaScript** e **MySQL**. O sistema permite o cadastro, edição, exclusão e busca de clientes, bem como a visualização dos dados de cada cliente .

## Tecnologias Utilizadas

- **Backend**: Java, Spring Boot, Hibernate
- **Frontend**: HTML, CSS, JavaScript, Bootstrap, jQuery
- **Banco de Dados**: MySQL
- **Frameworks e Bibliotecas**:
  - **Spring Boot**: Para a construção de APIs RESTful e gerenciamento do servidor.
  - **Hibernate**: Para o mapeamento objeto-relacional (ORM).
  - **Thymeleaf**: Para renderização das páginas HTML no backend.
  - **Bootstrap**: Para design responsivo.
  - **jQuery**: Para interatividade no frontend.

## Estrutura do Projeto

A estrutura do projeto está organizada da seguinte forma:

comercial/ # Controladores que processam as requisições HTTP │ │ │ ├── dao/ # Acesso ao banco de dados (DAO) │ │ │ ├── model/ # Modelos (entidades do banco de dados) │ │ │ └── service/ # Lógica de negócios │ │ ├── resources/ │ │ │ ├── static/ # Arquivos estáticos (CSS, JS) │ │ │ └── templates/ # Templates HTML (Thymeleaf) │ │ ├── application.properties # Configurações do Spring Boot ├── pom.xml # Dependências do Maven └── README.md # Este arquivo


## Dependências

O projeto utiliza o Maven para gerenciamento de dependências. As principais dependências do `pom.xml` são:

- **Spring Boot Starter Web**: Para criar e gerenciar o servidor e endpoints RESTful.
- **Spring Boot Starter Thymeleaf**: Para renderizar páginas HTML no backend.
- **Spring Boot Starter Data JPA**: Para trabalhar com o banco de dados usando Hibernate.
- **MySQL Connector/J**: Para comunicação com o banco de dados MySQL.
- **Spring Boot Starter Validation**: Para validação de dados de entrada.
- **Bootstrap e jQuery**: Para facilitar a criação de interfaces de usuário responsivas e interativas.

### Dependências no `pom.xml`

```xml
<dependencies>
    <!-- Spring Boot Starter Web (REST APIs e servidor) -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>

    <!-- Spring Boot Starter Data JPA (Hibernate ORM) -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>

    <!-- Thymeleaf (Renderização de páginas HTML) -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-thymeleaf</artifactId>
    </dependency>

    <!-- MySQL Connector -->
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
    </dependency>

    <!-- Spring Boot Starter Validation (Validação de dados) -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-validation</artifactId>
    </dependency>

    <!-- Bootstrap (CSS e design responsivo) -->
    <dependency>
        <groupId>org.webjars</groupId>
        <artifactId>bootstrap</artifactId>
        <version>5.0.0</version>
    </dependency>

    <!-- jQuery (Interatividade no frontend) -->
    <dependency>
        <groupId>org.webjars</groupId>
        <artifactId>jquery</artifactId>
        <version>3.6.0</version>
    </dependency>
</dependencies>

Configurações
Configuração do Banco de Dados
Para que o projeto funcione corretamente, você precisa configurar o banco de dados MySQL e as credenciais de conexão no arquivo src/main/resources/application.properties.

Exemplo de configuração de banco de dados:

spring.datasource.url=jdbc:mysql://localhost:3306/comercio_sa
spring.datasource.username=root
spring.datasource.password=sua-senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

spring.datasource.url : URL de conexão com o banco de dados MySQL.
spring.datasource.username : Nome de usuário do MySQL.
spring.datasource.password : Senha do MySQL.
spring.jpa.hibernate.ddl-auto : Configuração para geração automática de esquema de banco de dados.
spring.jpa.show-sql : Exibe como consultas SQL no console.

Como Executar o Projeto
Pré-requisitos
Java 11 ou superior
MySQL 8.0 ou superior
Maven (se não estiver usando o wrapper do Maven)

Passos para Rodar o Sistema
Clone o Repositório :

Clone o repositório do projeto:
git clone https://github.com/seu-usuario/comercio-sa.git
Entre no Diretório do Projeto :

Acesse o diretório do projeto:
cd comercio-sa
Configuração do Banco de Dados :

Crie o banco de dados comercio_sano MySQL (se ainda não existeem).

Execute o script SQL schema.sqlno MySQL para criar as tabelas e popular o banco.

Compilação e Execução :

Utilize o Maven para compilar e rodar o projeto:

./mvnw spring-boot:run
Ou, caso tenha o Maven instalado globalmente:
mvn spring-boot:run

Acesse o Sistema :

O sistema estará disponível no seu navegador, acessando:
http://localhost:8080
