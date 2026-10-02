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
   garçom["garçom"]

    %% ações
    subgraph sistema
        comida["pedir comida"]
        vinho["pedir vinho"]
    end

    %% relacionamento
    cliente -- "faz pedido" --- comida
    garçom -- "recebe pedido" --- comida

    vinho -. "estende" .-> comida
```
### Diagrama de Classe 

```mermaid
classDiagram
    class Veterinarios {
           %% atributos: caracteristicas que serao
        %% armazenados no sistema
      -CPF: string
      %% metodos: acoes que serao desempenhadas
      %% por essa entidade no sistema 
      +darCPF() string
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
    -Animais: Lista de Animais
    -Motivo Consulta:string
    +Informar Motivo Consulta() string
    }

```
