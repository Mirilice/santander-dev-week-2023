# Santander Dev Week 2023

Java RESTful API criada para a Santander Dev Week.

## Principais Tecnologias
 - **Java 17**: Utilizaremos a versão LTS mais recente do Java para tirar vantagem das últimas inovações que essa linguagem robusta e amplamente utilizada oferece;
 - **Spring Boot 3**: Trabalharemos com a mais nova versão do Spring Boot, que maximiza a produtividade do desenvolvedor por meio de sua poderosa premissa de autoconfiguração;
 - **Spring Data JPA**: Exploraremos como essa ferramenta pode simplificar nossa camada de acesso aos dados, facilitando a integração com bancos de dados SQL;
 - **OpenAPI (Swagger)**: Vamos criar uma documentação de API eficaz e fácil de entender usando a OpenAPI (Swagger), perfeitamente alinhada com a alta produtividade que o Spring Boot oferece;
 - **Railway**: facilita o deploy e monitoramento de nossas soluções na nuvem, além de oferecer diversos bancos de dados como serviço e pipelines de CI/CD.

## [Link do Figma](https://www.figma.com/file/0ZsjwjsYlYd3timxqMWlbj/SANTANDER---Projeto-Web%2FMobile?type=design&node-id=1421%3A432&mode=design&t=6dPQuerScEQH0zAn-1)

O Figma foi utilizado para a abstração do domínio desta API, sendo útil na análise e projeto da solução.


## Diagrama de Classes (Domínio da API)

```mermaid
classDiagram
  class Usuario {
    -String nome
    -Conta conta
    -Recurso[] recursos
    -Cartao cartao
    -Novidades[] novidades
  }

  class Conta {
    -String numero
    -String agencia
    -Number saldo
    -Number limite
  }

  class Recurso {
    -String icone
    -String descricao
  }

  class Cartao {
    -String numero
    -Number limite
  }

  class Novidades {
    -String icone
    -String descricao
  }

  Usuario "1" *-- "1" Conta
  Usuario "1" *-- "N" Recurso
  Usuario "1" *-- "1" Cartao
  Usuario "1" *-- "N" Novidades
```

 👊🤩
