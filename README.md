# Desafio POO - iPhone

Projeto desenvolvido para o Desafio JAVA POO - Modelagem e Diagramação de um Componente iPhone - DIO SANTANDER DEV WEEK 2024

Este projeto modela e implementa as funcionalidades básicas do iPhone de 2007, incluindo Reprodutor Musical, Aparelho Telefônico e Navegador na Internet.

## Estrutura do Projeto

- `ReprodutorMusical.java`: Interface para o reprodutor musical.
- `AparelhoTelefonico.java`: Interface para o aparelho telefônico.
- `NavegadorNaInternet.java`: Interface para o navegador na internet.
- `iPhone.java`: Classe que implementa todas as interfaces acima.

## Diagrama UML (Mermaid)

```mermaid
classDiagram
    class iPhone {
        +void tocar()
        +void pausar()
        +void selecionarMusica(String musica)
        +void ligar(String numero)
        +void atender()
        +void iniciarCorreioVoz()
        +void exibirPagina(String url)
        +void adicionarNovaAba()
        +void atualizarPagina()
    }

    class ReprodutorMusical {
        <<interface>>
        +void tocar()
        +void pausar()
        +void selecionarMusica(String musica)
    }

    class AparelhoTelefonico {
        <<interface>>
        +void ligar(String numero)
        +void atender()
        +void iniciarCorreioVoz()
    }

    class NavegadorNaInternet {
        <<interface>>
        +void exibirPagina(String url)
        +void adicionarNovaAba()
        +void atualizarPagina()
    }

    iPhone ..|> ReprodutorMusical
    iPhone ..|> AparelhoTelefonico
    iPhone ..|> NavegadorNaInternet
```

![Diagrama UML](diagrama_uml.png)

## Como Compilar e Executar

1. Compile as classes Java:
   ```sh
   javac ReprodutorMusical.java AparelhoTelefonico.java NavegadorNaInternet.java iPhone.java
   ```

2. Execute a classe `iPhone`:
   ```sh
   java iPhone
   ```

## Funcionalidades

### Reprodutor Musical:
- `void tocar()`: Inicia a reprodução de uma música.
- `void pausar()`: Pausa a reprodução de uma música.
- `void selecionarMusica(String musica)`: Seleciona uma música específica para tocar.

### Aparelho Telefônico:
- `void ligar(String numero)`: Faz uma chamada para o número fornecido.
- `void atender()`: Atende uma chamada recebida.
- `void iniciarCorreioVoz()`: Inicia o correio de voz.

### Navegador na Internet:
- `void exibirPagina(String url)`: Exibe a página web fornecida pela URL.
- `void adicionarNovaAba()`: Adiciona uma nova aba no navegador.
- `void atualizarPagina()`: Atualiza a página atual do navegador.

## Exemplo de Uso

```java
public class Main {
    public static void main(String[] args) {
        iPhone meuIphone = new iPhone();

        // Testando ReprodutorMusical
        meuIphone.selecionarMusica("Imagine");
        meuIphone.tocar();
        meuIphone.pausar();

        // Testando AparelhoTelefonico
        meuIphone.ligar("123456789");
        meuIphone.atender();
        meuIphone.iniciarCorreioVoz();

        // Testando NavegadorNaInternet
        meuIphone.exibirPagina("https://www.example.com");
        meuIphone.adicionarNovaAba();
        meuIphone.atualizarPagina();
    }
}
```

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.


## Estrutura do Repositório

```
dio-desafio-poo-iphone/
├── src/
│   ├── ReprodutorMusical.java
│   ├── AparelhoTelefonico.java
│   ├── NavegadorNaInternet.java
│   ├── iPhone.java
│   ├── diagrama_uml.png
│   └── README.md
```


## Contato

Para mais informações, entre em contato através do email: mario@gmail.com

**Meu Perfil na DIO:** [https://www.dio.me/users/mariojbe](https://www.dio.me/users/mariojbe)

<br>
Developed by Mário Evangelista
