# Alguns comandos do MarkDown extendido (RFC 7764)


## CheckList

- [ ] Bater o ponto
- [ ] Abrir o Feedz
- [x] Pegar café

## Bloco de código (fences)

```{.py3 linenums="3" hl_lines="2-4" title="código de teste.php"}
$i = 0;
while ($i < 5){
$i++;
echo "ô vida boa"
}
```

## Alterações de texto

Emoji: :coffee:

~~texto tachado~~

==texto realçado==

## Admonitions

!!! note

    Sou uma nota!

!!! abstract

    Sou um abstrato!

!!! info

    Sou uma informação!

!!! tip

    Sou uma dica!

!!! success

    Sou um sucesso!

!!! question

    Sou uma pergunta!

!!! warning

    Sou um aviso!

!!! failure

    Sou uma falha!

!!! danger

    Sou um perigo!

!!! bug

    Sou um bug!

!!! example

    Sou um exemplo!

!!! quote

    Sou uma citação!


Conteúdo expandível:

??? tip "eu renderizo..."

    fechado

???+ tip "eu renderizo..."

    aberto


Esconder título

!!! tip ""

    Sou conteúdo! Sed vehicula congue mattis. Duis nec molestie ante, nec imperdiet dui. Integer dignissim, sem sed rutrum euismod, urna erat auctor sapien, sit amet ullamcorper magna turpis ac odio. Morbi in malesuada lorem. Curabitur feugiat dolor nulla, vitae semper nulla gravida eu.

!!! info inline end "Eu renderizo no canto da página!"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam egestas orci ut libero congue, in bibendum sem ultrices. Morbi porta ex sed est venenatis mattis. Nulla quis quam nibh.

## Tabelas

Tabela para a direita:

| Nome | Idade |
| ----: | ----: |
| Diego | 18 |
| Peres | 24 |
| Eduarda | 22 |

Tabela centralizada

| Method      | Description                          |
| :-----------: | :------------------------------------: |
| GET       | :material-check:     Fetch resource  |
| PUT       | :material-check-all: Update resource |
| DELETE    | :material-close:     Delete resource |

## Inserir teclas:

++ctrl+alt+del++

## Diagramas (Implementação padrão do mermaid com JS)

Flowcharts:

``` mermaid
graph LR
  A[Start] --> B{Error?};
  B -->|Yes| C[Hmm...];
  C --> D[Debug];
  D --> B;
  B ---->|No| E[Yay!];
```

Diagrama de sequência:

``` mermaid
sequenceDiagram
  autonumber
  Alice->>John: Hello John, how are you?
  loop Healthcheck
      John->>John: Fight against hypochondria
  end
  Note right of John: Rational thoughts!
  John-->>Alice: Great!
  John->>Bob: How about you?
  Bob-->>John: Jolly good!
```

Diagrama de transição de estados:

``` mermaid
stateDiagram-v2
  state fork_state <<fork>>
    [*] --> fork_state
    fork_state --> State2
    fork_state --> State3

    state join_state <<join>>
    State2 --> join_state
    State3 --> join_state
    join_state --> State4
    State4 --> [*]
```

Diagrama de classe:

``` mermaid
classDiagram
  Person <|-- Student
  Person <|-- Professor
  Person : +String name
  Person : +String phoneNumber
  Person : +String emailAddress
  Person: +purchaseParkingPass()
  Address "1" <-- "0..1" Person:lives at
  class Student{
    +int studentNumber
    +int averageMark
    +isEligibleToEnrol()
    +getSeminarsTaken()
  }
  class Professor{
    +int salary
  }
  class Address{
    +String street
    +String city
    +String state
    +int postalCode
    +String country
    -validate()
    +outputAsLabel()  
  }
```

Diagrama de relacionamento de identidade:

``` mermaid
erDiagram
  CUSTOMER ||--o{ ORDER : places
  ORDER ||--|{ LINE-ITEM : contains
  LINE-ITEM {
    string name
    int pricePerUnit
  }
  CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

## Anotações em code blocks

``` yaml
theme:
  features:
    - content.code.annotate # (1)
```

1.  Eu sou uma anotação! Posso conter texto, código adicional, imagens, links, etc.
