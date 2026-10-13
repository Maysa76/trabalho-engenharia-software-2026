# trabalho-engenharia-software-2026
Trabalho de clínica veterinária do Técnico em Informática, segundo semestre de 2026.

Link do projeto do Figma:
https://www.figma.com/proto/daZmTMeXfA2XVBkE5mni0Y/meu-projeto?node-id=145-332&starting-point-node-id=145%3A332&t=9yZ8tkHPclGnqlpo-1

## Diagrama UML 

### Diagramas de caso de uso

```mermaid
flowchart TD
    %% atores
   cliente["cliente"]
   veterinario["veterinario"]

    %% ações
    subgraph sistema
        informações["motivo consulta"]
        motivo["pedir informações"]
    end

    %% relacionamento
    cliente -- "informar informações" --- informações
    veterinario-- "pedir informações" --- informações

    motivo-. "estende" .-> informações
```
### Diagrama de Classe 

```mermaid
classDiagram
    class Veterinarios {
           %% atributos: caracteristicas que serao
        %% armazenados no sistema
      -nome: string
      -sobrenome: string
      -telefone: string
      -Email: string
      -Consultas: string 
      -Lista Pessoas/Cliente: string
      - Nome do Pet: string
      -Raça: string
      -Peso do animal: float
      -Idade do animal 
      - Motivo da Consulta : string
      - teve Febre : string
      - Datas das vacinas : string
      - Doenças anteriores : string
      - Outras infomações: string

      %% metodos: acoes que serao desempenhadas
      %% por essa entidade no sistema 
      +Pedir nome() string
      +Pedir sobrenome() string
      +Pedir contato() string
      +Pedir Email() string
      +Pedir Nome do Pet() string
      +Pedir Raça() string
      +Pedir Peso do animal() float
      +Idade do animal () string
      + Motivo da Consulta ()
      + teve Febre () string
      + Datas das vacinas () string
      + Doenças anteriores () string
      +atender Animal(animal: Animal): void
    }

    Veterinarios -- Animal 
     Animal -- Cliente
    
    class Animal {
        -dono: Cliente
        -Nome: string
        -Raça: string
        -Sexo: string
        -Peso: Float
        -datas Vacinas: string
    
    }
     
    class Cliente {
    -Animais: Lista de Animais ()
    -Motivo Consulta:string
    -nome cliente: string
    -sobrenome cliente: string
    -telefone Cliente: string
    -Email cliente: string

    +Informar Motivo Consulta() string
     +informar nome() string
      +informar sobrenome() string
      +informar contato() string
      +Informar Email() string
      +Informar Nome do Pet() string
      +Informar Raça() string
      +Informar Peso do animal() float 
      + Informar Idade do animal () string
      + Informar Motivo da Consulta ()
      + Informar teve Febre () string
      + Informar Datas das vacinas () string
      + Informar Doenças anteriores () string

    }
```
