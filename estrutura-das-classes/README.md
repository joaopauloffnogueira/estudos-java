# Guia Básico de Estruturação de Código em Java

Imagine que escrever código é como montar um castelo com blocos de LEGO. Cada peça tem um formato específico e um papel importante para que o castelo fique bonito e forte. No Java, essas “peças” são palavras reservadas e convenções que ajudam a criar programas claros e organizados.

> Observação: Muitos projetos recomendam escrever o código em inglês para padronização.
> 

---

## 1. Criando e Organizando Classes

### Declaração de uma Nova Classe

Para começar, você cria uma **classe**, que é como um molde para seus objetos. A estrutura básica é:

```java
java
CopiarEditar
public class MinhaClass {
    // Seu código vai aqui
}

```

**O que cada parte faz?**

- **public:** Permite que a classe seja usada por qualquer parte do programa.
- **class:** Informa que estamos definindo uma nova classe.
- **MinhaClass:** É o nome que identifica a classe – pense nele como o nome do seu castelo.
- **{ } (chaves):** Delimitam onde o conteúdo da classe será escrito.

> Dica de estilo: A documentação oficial recomenda que o nome da classe comece com letra maiúscula e seja escrito de forma contínua (por exemplo, MinhaClasse).
> 

---

## 2. O Método Main: A Porta de Entrada do Programa

Toda aplicação executável em Java precisa ter um método especial chamado **main**. Esse método é como a porta principal do castelo: é por onde o programa começa a funcionar.

```java
java
CopiarEditar
public class MinhaClass {
    public static void main(String[] args) {
        // Código que inicia o programa
    }
}

```

**Detalhando cada parte:**

- **public:** A classe pode ser acessada de qualquer lugar.
- **static:** O método pertence à classe em si, não a objetos individuais.
- **void:** Significa que o método não retorna nenhum valor.
- **main:** É o nome do método que inicia a execução do programa.
- **String[] args:** Um conjunto (array) de textos que podem ser passados ao iniciar o programa.

*Analogia:* Pense no método **main** como a chave que abre a porta de entrada do seu castelo, permitindo que o programa "ganhe vida".

---

## 3. Imprimindo Mensagens na Tela

Para mostrar mensagens ao usuário, o Java usa a classe **System** com seu membro **out**. O comando de impressão é simples:

```java
java
CopiarEditar
public class MinhaClass {
    public static void main(String[] args) {
        System.out.print("Olá Mundo!");
    }
}

```

**Explicação:**

- **System.out:** É como um megafone que envia sua mensagem para a tela.
- **print:** O comando que "fala" a mensagem no terminal.

Após escrever o código, basta clicar em "Run" na sua IDE. O sistema compilará o código e exibirá o resultado, assim como ver um desenho que você montou com seus blocos de LEGO.

---

## 4. Padrões de Nomenclatura: Dando Nome aos Seus Blocos

Assim como é importante nomear seus brinquedos de forma clara, a escrita do código também exige nomes bem definidos para arquivos, classes e variáveis.

### Arquivos e Classes

- **Arquivos `.java`:**
    - Devem começar com letra **maiúscula**.
    - Se o nome for composto, cada palavra inicia com letra maiúscula.*Exemplos:* `Calculadora.java`, `CalculadoraCientifica.java`.
- **Nome da classe no arquivo:**
    - A classe deve ter o mesmo nome do arquivo.
    
    ```java
    java
    CopiarEditar
    // Em CalculadoraCientifica.java
    public class CalculadoraCientifica {
        // Código da classe
    }
    
    ```
    

### Variáveis

- **CamelCase:**
    - As variáveis começam com **letra minúscula**.
    - Se forem compostas, a primeira letra da segunda palavra é **maiúscula**.*Exemplo:*
    
    ```java
    java
    CopiarEditar
    var anoFabricacao = 1995;
    
    ```
    
- **Constantes:**
    - Se o valor não deve mudar, use `final` e escreva em **letras maiúsculas**.*Exemplo:*
    
    ```java
    java
    CopiarEditar
    final String BR = "Brasil";
    
    ```
    

---

## 5. Regras para Nomeclatura de Variáveis

Na hora de criar nomes para variáveis, há regras a seguir – como se estivéssemos escolhendo um nome para um novo brinquedo:

- Pode conter apenas letras, _ (underline), $ e números (0 a 9).
- Deve começar com uma letra, _ ou $ (nunca com número).
- **Boa prática:** Começar com letra minúscula.
- Não pode ter espaços e não pode usar palavras reservadas da linguagem.
- Cada nome deve ser único dentro do mesmo escopo.

**Exemplos de declarações inválidas:**

```java
java
CopiarEditar
int numero&um = 1;
int 1numero = 1;
int numero um = 1;
int long = 1;

```

**Exemplos de declarações válidas:**

```java
java
CopiarEditar
int numero$um = 1;
int numero1 = 1;
int numeroum = 1;
int longo = 1;

```

*Analogia:* É como escolher um nome para seu cachorro – deve ser único e seguir certas regras (não pode ter espaços ou números no começo).

---

## 6. Declarando Variáveis e Métodos

### Variáveis

Declarar uma variável é como dizer: "Eu tenho um balde para guardar um número ou uma palavra." A estrutura básica é:

```java
java
CopiarEditar
int idade = 23;
double altura = 1.62;
Dog spike; // Declaração sem atribuição imediata

```

### Métodos

Um método é como uma receita de bolo, que explica passo a passo como fazer algo. A estrutura para declarar um método é:

```java
java
CopiarEditar
int somar(int numeroUm, int numeroDois) {
    // Código para somar
}

String formatarCep(long cep) {
    // Código para formatar um CEP
}

```

### Exemplo Completo:

```java
java
CopiarEditar
public class MinhaClasse {
    public static void main(String[] args) {
        String primeiroNome = "João";
        String segundoNome = "Paulo";

        String nomeCompleto = nomeCompleto(primeiroNome, segundoNome);
        System.out.println(nomeCompleto);
    }

    public static String nomeCompleto(String primeiroNome, String segundoNome) {
        return "Resultado do método " + primeiroNome.concat(" ").concat(segundoNome);
    }
}

```

*Analogia:* Variáveis são como caixas onde você guarda coisas, e métodos são como instruções de como usar essas caixas para realizar tarefas.

---

## 7. Indentação: Organizando o Código

Indentação significa colocar espaços ou tabulações para organizar o código de forma hierárquica, facilitando a leitura – é como arrumar seus brinquedos em caixas para saber onde cada um está.

### Sem Identação:

```java
java
CopiarEditar
int mediaFinal = 6;
if(mediaFinal < 6)
System.out.println("Reprovado");
else if(mediaFinal == 6)
System.out.println("Prova Minerva");
else
System.out.println("Aprovado");

```

### Com Identação:

```java
java
CopiarEditar
int mediaFinal = 6;
if (mediaFinal < 6)
    System.out.println("Reprovado");
else if (mediaFinal == 6)
    System.out.println("Prova Minerva");
else
    System.out.println("Aprovado");

```

*Analogia:* A indentação é como alinhar seus lápis em uma caixa: quando estão organizados, fica muito mais fácil encontrar o que você precisa.

---

## 8. Organização de Arquivos: Arrumando a Casa do Projeto

Conforme seu programa (ou castelo) vai crescendo, novos arquivos são criados. Para manter tudo organizado, usa-se a **organização em pacotes (packages)**. Isso é parecido com ter diferentes cômodos para diferentes brinquedos.

### Tipos de Projetos e Pacotes

| Tipo de Projeto | Sufixo do Pacote |
| --- | --- |
| comercial | com |
| organizacional | org |
| opensource | org |
| educacional | edu |
| governamental | gov |
| serviços de internet | net |
| militar | mil |
| informativo | info |
| projetos de negócios | biz |

### Exemplos de Estruturas de Pastas

### Estrutura Simples

```java
java
CopiarEditar
projeto-java/
├── src/
│   ├── edu/
│   │   ├── joao/
│   │       ├── primeirasemana/
│   │       │   └── MinhaClasse.java
│   │       ├── segundasemana/
│   │           └── Boletim.java
├── README.md

```

### Estrutura Avançada

```java
java
CopiarEditar
HyperTech/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── hypertech/
│   │   │           └── notification/
│   │   │               ├── app/
│   │   │               │   └── Application.java
│   │   │               ├── model/
│   │   │               │   └── Notification.java
│   │   │               ├── service/
│   │   │               │   └── NotificationService.java
│   │   ├── resources/
│   │       └── application.properties
│   ├── test/
│       ├── java/
│       │   └── com/
│       │       └── hypertech/
│       │           └── notification/
│       │               ├── app/
│       │               │   └── ApplicationTest.java
│       │               ├── model/
│       │               │   └── NotificationTest.java
│       │               ├── service/
│       │                   └── NotificationServiceTest.java
│       ├── resources/
├── lib/
├── bin/
├── build/
├── docs/
├── config/
├── scripts/
└── resources/

```

*Analogia:* Organizar os arquivos do projeto é como arrumar seu quarto, onde cada brinquedo tem um lugar específico para que você encontre tudo facilmente.

---

## 9. JavaBeans: Boas Práticas para um Código Legível

JavaBeans é um conjunto de convenções que ajuda a tornar o código mais organizado e fácil de entender. Essas regras facilitam a manutenção do programa, tanto para você quanto para sua equipe.

### Variáveis

**Sugestões importantes:**

- **Clareza:** Use nomes completos, sem abreviações ou termos confusos.
- **Singularidade:** Use o singular para uma variável que guarda um único valor. Use o plural somente para arrays ou coleções.
- **Idioma Consistente:** Se escolher escrever em inglês, mantenha todos os nomes nessa língua.

**Exemplos não recomendados:**

```java
java
CopiarEditar
double salMedio = 1500.23;
String emails = "aluno@escola.com";
String myName = "JOSEPH";

```

**Exemplos recomendados:**

```java
java
CopiarEditar
double salarioMedio = 1500.23;
String email = "aluno@escola.com";
String[] emails = {"aluno@escola.com", "professor@escola.com"};
String meuNome = "JOSEPH";

```

### Métodos

Métodos devem ser nomeados como verbos e escritos em letras minúsculas, com a primeira letra de cada palavra subsequente em maiúscula (exceto a primeira palavra).

**Exemplos de nomes de métodos:**

```java
java
CopiarEditar
somar(int n1, int n2) { }
abrirConexao() { }
concluirProcessamento() { }
findById(int id) { }

```

*Analogia:* Pense nos métodos como ações que você pode realizar, como "pular" ou "correr". O nome do método deve dizer exatamente o que ele faz.

---

## Considerações Finais

Este guia foi estruturado para mostrar, de forma simples e clara, como construir programas em Java, seguindo as convenções recomendadas na documentação oficial. Assim como organizar seus brinquedos ou montar um castelo com blocos de LEGO, a clareza e a organização no código ajudam a manter seu projeto compreensível e fácil de manter no futuro.

Explore e pratique cada tópico para dominar a arte de programar em Java!