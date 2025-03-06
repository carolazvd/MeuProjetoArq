# Projeto - Spring Boot

Este é um projeto simples utilizando o framework **Spring Boot** para criar uma aplicação web RESTful que retorna uma mensagem "Hello, World!" quando a URL `/test` é acessada.

## Estrutura do Projeto

O projeto consiste em duas classes principais:

1. **`HelloController`**: Esta classe é um controlador REST que responde a requisições HTTP GET na URL `/test` e retorna a mensagem "Hello, World!".
   
2. **`DemoApplication`**: A classe principal que inicializa a aplicação Spring Boot.

### HelloController

```java
package com.seuprojeto.controller.demo;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping("/test")
    public String helloWorld() {
        return "Hello, World!";
    }
}
