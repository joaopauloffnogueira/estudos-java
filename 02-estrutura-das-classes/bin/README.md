# Exercícios

---

# JAVA

# **#Exercício 01**

Explique os principais elementos que compõem a estrutura de uma classe Java e, em especial, o papel do método `main`.

```java
public class MinhaClass {
		
}
```

- **public:**
- **class**:
- **MinhaClass**:
- **Chaves** `{}`:

- Resposta
    - **public:** indica que a classe é pública e pode ser acessada por qualquer pessoa.
    - **class**: define que estamos criando uma classe.
    - **MinhaClass**: nome que identifica a classe.
    - **Chaves** `{}`: delimitam onde o código da classe será escrito.

```java
public class MinhaClass {
		public static void main (String [] args){
					
		}
}
```

- **public:**
- **static:**
- **void:**
- **main:**
- **parâmetro ():**
- **String:**
- **[ ] args (argumento/parâmetro):**

- Resposta
    - **public:** indica que a classe é pública e pode ser acessada por qualquer pessoa.
    - **static:** Define que o método ou variável pertence à classe e não a instâncias específicas.
    - **void:** Tipo de retorno que indica que o método não retorna nenhum valor.
    - **main:** Método principal que serve como ponto de entrada para a execução de um programa Java.
    - **parâmetro ():** Refere-se aos parâmetros que um método pode receber.
    - **String:**  Tipo de dados que representa uma sequência de caracteres. Em Java, **String** é uma classe.
    - **[ ] args (argumento/parâmetro):**  Array de strings que representa os argumentos de linha de comando passados para o método **main**.

---

# **#Exercício 02**

Crie um arquivo Java com o nome `MinhaPrimeiraClasse.java` que contenha:

- Uma classe pública chamada `MinhaPrimeiraClasse`.
- O método `main` que, ao ser executado, imprima a mensagem `Olá Mundo!` no console.

- Resposta
    
    ```java
    public class MinhaPrimeiraClasse {
    		public static void main (String [] args){
    				System.out.print("Olá Mundo!")
    		}
    }
    ```
    

---

# **#Exercício 03**

Qual é a forma correta de nomear uma classe e variável no JAVA?

- **Variável:**
- Resposta
    
    ```java
    var anoFabricacao = 1995;
    ```
    

- **Classe:**
- Resposta
    
    ```java
    public class MinhaClass {}
    ```
    

- **Variável Constante:**
- Resposta
    
    ```java
    final String BR = "Brasil"
    ```
    

---

# **#Exercício 04**

Faça uma estrutura de pastas e arquivos simples.

- Resposta
    
    ```java
    projeto-java > src > edu > estudos-java > 
    01-introducao-java > Introducao.java
    02-estrutura-java > Estrutura.java
    ```
    

---