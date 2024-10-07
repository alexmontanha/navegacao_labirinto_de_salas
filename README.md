# Atividade Prática - Busca em Labirinto

## **Problema: Navegação em um Labirinto de Salas**

Você é responsável por criar um algoritmo para ajudar um robô a navegar por um labirinto de salas conectadas. Cada sala está conectada a uma ou mais outras salas, mas o robô não sabe inicialmente qual é o caminho certo para chegar à **sala de saída**. Sua tarefa é implementar um algoritmo de **busca** para encontrar um caminho que o robô possa seguir até essa sala de saída.

## **Contexto do Problema**

O labirinto é representado como um **grafo**, onde cada sala é um **nó** e cada passagem entre salas é uma **aresta**. O robô começa em uma sala inicial, e sua meta é chegar a uma sala específica que contém a saída. As salas estão conectadas de forma que, a partir de uma sala, o robô pode se mover para qualquer sala diretamente conectada a ela.

### Regras

- O robô pode se mover de uma sala para outra apenas se houver uma passagem entre elas.
- O robô não sabe previamente qual o caminho correto e precisa explorar diferentes salas para encontrar a saída.
- O labirinto **não tem ciclos** (ou seja, não existe um caminho que leve de volta a uma sala já visitada).
  
### Objetivo

O robô deve encontrar um **caminho** da sala de início até a sala de saída.

## **Instruções**

1. **Entrada**:
   - Um grafo representando o labirinto, onde as **salas são nós** e as **passagens entre salas são arestas**.
   - Uma sala de **início** (onde o robô começa).
   - Uma sala de **saída** (onde o robô deve chegar).

2. **Saída**:
   - O algoritmo deve retornar o **caminho** da sala de início até a sala de saída.
   - Se não houver caminho possível, o algoritmo deve retornar `None`.

## **Tarefas**

- Implemente uma função chamada `encontrar_caminho(grafo, inicio, saida)` que realiza a busca pelo caminho.
- Utilize um algoritmo de **Busca em Largura (BFS)** ou **Busca em Profundidade (DFS)** para encontrar o caminho.
  
## **Exemplo de Representação de Entrada**

O labirinto pode ser representado assim:

```python
labirinto = {
    'Sala 1': ['Sala 2', 'Sala 3'],
    'Sala 2': ['Sala 4'],
    'Sala 3': ['Sala 4', 'Sala 5'],
    'Sala 4': ['Sala 6'],
    'Sala 5': ['Sala 6'],
    'Sala 6': []  # Sala de saída
}
```

Neste caso:

- **Sala 1** é a sala inicial.
- **Sala 6** é a sala de saída.

## **Exemplo de Execução**

```python
def encontrar_caminho(labirinto, inicio, saida):
    # Sua implementação vai aqui
    pass

# Chamando a função com os dados do labirinto
inicio = 'Sala 1'
saida = 'Sala 6'
caminho = encontrar_caminho(labirinto, inicio, saida)

print(f"Caminho encontrado: {caminho}")
```

Se houver um caminho, a saída pode ser algo como:

```python
Caminho encontrado: ['Sala 1', 'Sala 3', 'Sala 5', 'Sala 6']
```

## **Dicas**

- Lembre-se de usar uma estrutura de dados para armazenar as salas já visitadas, para evitar repetir a exploração de uma mesma sala.
- Teste seu código com diferentes configurações de labirintos, com mais ou menos salas e conexões.
