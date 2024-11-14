
# Cadastro Cliente

Este projeto foi desenvolvido como uma forma de estudo e prática, focando no cadastro de alunos utilizando a linguagem Java. O objetivo principal é aperfeiçoar os conhecimentos adquiridos e aplicar conceitos de programação de maneira prática e eficiente. A aplicação permite a criação, leitura, atualização e exclusão de registros de alunos, proporcionando uma experiência completa de gerenciamento de dados.


## Autores

- [@PabloVinicius](https://www.github.com/PabloViniciusSS)


## Rodando localmente

Clone o projeto

```bash
  git clone https://github.com/PabloViniciusSS/cadastroclientes
```

É necessario ter o JDK instalado, foi utilizado o Maven para gerenciar os pacotes.

## Estrutura do projeto

/api_clientes_java/
├── .mvn/
│   └── wrapper/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── seu_usuario/
│   │   │           └── api_clientes/
│   │   │               ├── controller/
│   │   │               ├── model/
│   │   │               ├── repository/
│   │   │               └── service/
│   │   └── resources/
│   │       ├── static/
│   │       ├── templates/
│   │       └── application.yml
│   ├── test/
│       └── java/
│           └── com/
│               └── seu_usuario/
│                   └── api_clientes/
├── .gitattributes
├── .gitignore
├── README.md
├── mvnw
├── mvnw.cmd
└── pom.xml

- src/main/java/com/seu_usuario/api_clientes/: Contém o código-fonte principal do projeto.

- controller/: Contém os controladores da aplicação.

- model/: Contém as classes de modelo (entidades).

- repository/: Contém as interfaces de repositório para acesso ao banco de dados.

- service/: Contém as classes de serviço que implementam a lógica de negócios.

- src/main/resources/application.yml: éonde tem os arquivos de configurações

## Tecnologias

- Java
- Spring Data JPA 
- Spring Framework 
- Postgresql.

## Documentação da API (Obs: onde tem a {id} coloca o id do cliente, para excluir, atualizar ou pesquisar).

#### Retorna todos os Clientes:

```http
  GET: /clientes
```

#### Retorna um cliente especifico:

```http
  GET: /clientes/{id}
```

| Parâmetro   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `id` | `string` | **Obrigatório**. Id do Cliente|


#### Para criar novos clientes:

```http
  POST: /clientes
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `nome`      | `string` | **Obrigatório**. O Nome do Cliente |
| `cpf`      | `string` | **Obrigatório**. O CPF do Cliente |
| `bairro`      | `string` | **Obrigatório**. O bairro do Cliente |
| `dataDeNascimento`  | `string` | **Obrigatório**. A data de nascimento do Cliente |




#### Para atualizar um clientes:


```http
  PUT: /clientes/{id}
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `nome`      | `string` | **Obrigatório**. O Nome do Cliente |
| `cpf`      | `string` | **Obrigatório**. O CPF do Cliente |
| `bairro`      | `string` | **Obrigatório**. O bairro do Cliente |
| `dataDeNascimento`  | `string` | **Obrigatório**. A data de nascimento do Cliente |




#### Para deletar um clientes:


```http
  DEL: /clientes/{id}
```


| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `alunoId`      | `int` | **Obrigatório**. O Id do cliente |





## Variáveis de Ambiente

Para rodar esse projeto, você vai precisar adicionar o caminho do banco na pasta resource application.yml.


