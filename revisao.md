# 🧠 Mapa Mental de POO em Java

## 1. Introdução ao Java e Fundamentos

### 1.1. Java e a POO
* **O que é Java?** Linguagem Orientada a Objetos, com foco em segurança e robustez.
* **A Grande Ideia:** "Write Once, Run Anywhere" (Independência de plataforma).
* **JVM (Java Virtual Machine):** Interpreta o *bytecode* (`.class`) e garante a execução em qualquer sistema.

### 1.2. Estrutura Básica
* **Classe:** Todo o código reside dentro de uma classe (o modelo/estrutura).
* **Método `main`:** Ponto de entrada (início da execução) do programa.
* **Saída:** `System.out.println()` imprime texto no console.

### 1.3. Variáveis e Tipos
* **Tipos Primitivos:** `int`, `double`, `boolean`, `char`, etc. (Armazenam valores diretamente).
* **Tipos Não-Primitivos:** `String`, *Arrays*, Classes, Interfaces (São referências/objetos).
* **`var` (Java 10+):** Permite inferência de tipo para variáveis locais, para código mais limpo.

### 1.4. Operadores e Fluxo de Controle
* **Operadores Matemáticos:** `+`, `-`, `*`, `/`, `%` (Módulo).
* **Operadores Relacionais:** `==`, `!=`, `>`, `<`, `>=`, `<=` (Retornam `boolean`).
* **Operadores Lógicos:** `&&` (AND), `||` (OR), `!` (NOT).
* **Decisão:** `if`/`else if`/`else` e `switch` (que pode ser uma *expression* para retornar valor).
* **Repetição:** `for` (para iterações determinadas) e `while` (enquanto a condição for verdadeira).

## 2. O Coração da POO: Pilares e Conceitos

### 2.1. Classe e Objeto (Revisão)
* **Classe (Modelo):** Define a estrutura (`Atributos` e `Métodos`).
* **Objeto (Instância):** Uma instância concreta da classe, criada com `new`.

### 2.2. Pilar 1: Abstração
* **Conceito:** Focar no essencial e ignorar detalhes irrelevantes para o contexto.
* **Exemplo:** A representação de um objeto muda conforme quem o utiliza (Ex: Visão do Piloto vs. Policial sobre o Carro).

### 2.3. Pilar 2: Encapsulamento
* **Conceito:** Agrupar dados e comportamentos, protegendo o acesso direto aos dados.
* **Na Prática:** Usar `private` para atributos e `public` para métodos *getters/setters*.

### 2.4. Pilar 3: Herança
* **Conceito:** Permite que uma subclasse herde funcionalidades de uma superclasse, estabelecendo uma relação "**é um**".
* **Palavra-chave:** `extends` (para declarar a herança) e `super` (para referenciar a classe pai).

### 2.5. Pilar 4: Polimorfismo
* **Conceito:** Capacidade de um objeto se comportar de múltiplas formas ("Muitas Formas").
* **Sobreposição (*Overriding*):** Subclasse fornece implementação específica para um método da superclasse.
* **Sobrecarga (*Overloading*):** Vários métodos com o mesmo nome na mesma classe, mas com **parâmetros diferentes**.

### 2.6. Abstrações Avançadas
* **Classe Abstrata:** Molde parcial; **não pode ser instanciada**. Contém métodos **abstratos** (sem corpo, forçam implementação na subclasse) e concretos. Relação "**é um**".
* **Interface:** Um "**contrato**" de comportamento. Garante que classes que a implementam (`implements`) terão os métodos definidos. Relação "**sabe fazer**".

## 3. Implementação em Java: Collections (ArrayList)

### 3.1. ArrayList: Coleção Dinâmica
* **Definição:** Array redimensionável (`java.util.ArrayList`).
* **Vantagem:** O tamanho pode ser modificado, permitindo adicionar/remover elementos, diferente dos arrays básicos.
* **Criação:** É um objeto, então se usa a palavra-chave `new` (Ex: `ArrayList<String> carros = new ArrayList<>();`).

### 3.2. Operações Básicas
* `add(item)`: Adiciona um item.
* `get(index)`: Acede um item pelo índice.
* `set(index, item)`: Altera um item.
* `remove(index)`: Remove um item.
* `clear()`: Remove todos os elementos.
* `size()`: Retorna o número de elementos.
* `Collections.sort(lista)`: Ordena a lista (é uma classe auxiliar, precisa de `import java.util.Collections;`).

### 3.3. Iteração
* **Loop `for` tradicional:** Percorre usando o índice (`i < lista.size()`).
* **Loop `for-each` (Melhor prática):** Forma concisa para percorrer todos os elementos (Ex: `for (String i : cars)`).

***