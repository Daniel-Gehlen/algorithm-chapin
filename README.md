# Diagrama de Fluxo representando um algorítmo em Diagrama de Chapin

O tipo de gráfico utilizado no exemplo é um diagrama de fluxo, que é um dos tipos de gráficos suportados pela linguagem Mermaid. Especificamente, o gráfico de fluxo é criado com a diretiva graph, que define um gráfico de fluxo direcionado onde os nós (caixas) são conectados por setas que indicam a direção do fluxo.

Dentro do gráfico de fluxo, são usadas subgrafos (subgraph) para agrupar conjuntos de nós relacionados. Cada subgrafo pode conter nós individuais (como as caixas de notas e etapas do algoritmo neste caso) e textos explicativos.

Mermaid é uma linguagem de descrição de diagramas que permite criar vários tipos de diagramas, como diagramas de fluxo, diagramas de sequência, diagramas de Gantt, entre outros. É muito popular para criar diagramas em documentos Markdown, como aqueles usados em repositórios do GitHub ou em páginas wiki.

```mermaid
graph TD;
    subgraph "Algoritmo de Cálculo de Média"
        subgraph "Solicitação de Notas"
            EntradaNota1(N1: 7) & EntradaNota2(N2: 8) & EntradaNota3(N3: 6) & EntradaNota4(N4: 9);
            SolicitaçãoNotas[Solicitação de Notas]
        end
        subgraph "Cálculo da Média"
            CalculoMédia(Média);
            CálculoMédiaTexto["Cálculo da Média: (N1 + N2 + N3 + N4) / 4"]
        end
        subgraph "Exibição do Resultado"
            ExibiçãoResultado(R: 7.5);
            ExibiçãoResultadoTexto["Exibição do Resultado: Média"]
        end
        SolicitaçãoNotas --> CalculoMédia;
        CalculoMédia --> ExibiçãoResultado;
    end



```
