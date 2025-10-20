# 🧠 Mapa Mental - Foco em Programação Orientada a Objetos (POO)

## 1. Fundamentos e Princípios de Design

### 1.1. Classe vs. Objeto
* **Classe:** O modelo ou *blueprint* (planta). Define os atributos e métodos.
* **Objeto:** A instância concreta da classe, que ocupa espaço na memória.

### 1.2. Os 4 Pilares da POO

| Pilar | Conceito Central | Objetivo |
| :--- | :--- | :--- |
| **Abstração** | Focar no essencial e ignorar detalhes irrelevantes para o contexto. | Simplificar a complexidade. |
| **Encapsulamento** | Agrupar dados e proteger o acesso direto, controlando-o por métodos. | Proteger a integridade dos dados e expor apenas o necessário. |
| **Herança** | Mecanismo de reutilização de código que estabelece a relação "**é um**". | Reutilizar código e estender funcionalidades. |
| **Polimorfismo** | Capacidade de um objeto se comportar de múltiplas formas ("Muitas Formas"). | Múltiplas formas de comportamento para uma mesma interface. |

## 2. Abstrações Avançadas e Contratos

### 2.1. Classes Abstratas
* **Natureza:** Não podem ser instanciadas (objeto parcialmente pronto).
* **Conteúdo:** Podem ter métodos concretos e métodos `abstract` (sem implementação).
* **Uso:** Relação "**é um**" (Herança). Subclasses devem implementar os métodos abstratos.

### 2.2. Interfaces
* **Natureza:** Contrato de comportamento, apenas define o que a classe "sabe fazer".
* **Conteúdo:** Todos os métodos são implicitamente públicos e abstratos.
* **Uso:** Relação "**sabe fazer**" (`implements`). Permite que uma classe implemente múltiplos contratos.

## 3. Representações Gráficas (UML Básico)

Estas formas são cruciais para ler e desenhar diagramas de classes:

### 3.1. Relação de Herança (Generalização)
* **Conceito:** Subclasse estende a Superclasse.
* **Representação:** Seta sólida com uma **ponta triangular não preenchida (vazia)**.
* **Direção:** Aponta da **Subclasse** (Filho) para a **Superclasse** (Pai).
    * *Exemplo:* `Carro` &rarr; `Veiculo`.

### 3.2. Relação de Implementação (Interface)
* **Conceito:** Classe implementa o contrato de uma Interface.
* **Representação:** Seta tracejada (ou pontilhada) com uma **ponta triangular não preenchida (vazia)**.
* **Direção:** Aponta da **Classe Implementadora** para a **Interface**.

### 3.3. Relação de Associação (Uso/Referência)
* **Conceito:** Uma classe usa ou tem uma referência a outra (sem relação de parentesco). É a relação mais comum.
* **Representação:** Linha sólida simples entre as classes.

### 3.4. Relação de Composição (Losango Preenchido)
* **Conceito:** Um tipo forte de associação, onde o objeto "parte" **não pode existir** sem o objeto "todo". Representa a relação "**tem um**" forte (Propriedade).
* **Representação:** **Losango preenchido (sólido)** na extremidade da classe "todo" (o container), com uma linha ligando à classe "parte".
    * *Exemplo:* Um `Motor` (parte) é composto por um `Carro` (todo); o motor geralmente é destruído se o carro for destruído.

### 3.5. Relação de Agregação (Losango Vazio)
* **Conceito:** Um tipo fraco de associação "**tem um**", onde o objeto "parte" **pode existir** independentemente do objeto "todo".
* **Representação:** **Losango vazio (não preenchido)** na extremidade da classe "todo" (o container), com uma linha ligando à classe "parte".
    * *Exemplo:* Uma `Biblioteca` (todo) tem `Livros` (parte); um livro pode existir mesmo que a biblioteca feche.