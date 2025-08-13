# Implementação de Lista Encadeada em Python ⛓️

Este repositório contém uma implementação didática de uma **Lista Encadeada Simples** (Singly Linked List) em Python. O objetivo deste projeto é demonstrar de forma clara e comentada como essa estrutura de dados fundamental funciona, incluindo suas principais operações como inserção, busca e remoção.

Este código foi criado com fins educacionais, ideal para estudantes de Ciência da Computação, Engenharia de Software ou qualquer pessoa interessada em aprofundar seus conhecimentos em estruturas de dados.

---

## 🚀 Funcionalidades Implementadas

A classe `ListaEncadeada` possui os seguintes métodos:

* **`insere(data)`**: Insere um novo item no **início** da lista. (Complexidade: $O(1)$)
* **`insere_no_fim(data)`**: Insere um novo item no **final** da lista. (Complexidade: $O(n)$)
* **`insere_na_posicao(data, posicao)`**: Insere um novo item em uma **posição específica** (baseada em índice). (Complexidade: $O(n)$)
* **`buscar_elemento(data)`**: Busca um item pelo seu **valor** e retorna seu índice. Retorna `None` se não for encontrado. (Complexidade: $O(n)$)
* **`buscar_elemento_por_indice(indice)`**: Busca e retorna o **valor** de um item a partir de seu índice. Retorna `None` se o índice for inválido. (Complexidade: $O(n)$)
* **`remover_elemento(data)`**: Remove a primeira ocorrência de um item com base no seu **valor**. Retorna `True` se a remoção foi bem-sucedida e `False` caso contrário. (Complexidade: $O(n)$)

---

## 🛠️ Como Usar

O uso da estrutura é bastante simples. Primeiro, importe as classes e depois instancie um objeto `ListaEncadeada`. A partir daí, você pode chamar os métodos para manipular a lista.

### Exemplo de Código

```python
# 1. Crie uma instância da lista
lista = ListaEncadeada()

# 2. Insira elementos
lista.insere(10)          # Lista: 10
lista.insere(0)           # Lista: 0 -> 10
lista.insere_no_fim(20)   # Lista: 0 -> 10 -> 20
lista.insere_no_fim(40)   # Lista: 0 -> 10 -> 20 -> 40

# Insere o valor 30 na posição de índice 3
lista.insere_na_posicao(30, 3) # Lista: 0 -> 10 -> 20 -> 30 -> 40

# 3. Imprima a lista para ver o resultado
# O método __repr__ foi sobrecarregado para facilitar a visualização
print(lista)
# Saída esperada: 0 => 10 => 20 => 30 => 40 => None

# 4. Busque elementos
indice_do_20 = lista.buscar_elemento(20)
print(f"O elemento 20 está no índice: {indice_do_20}") # Saída: 2

valor_no_indice_4 = lista.buscar_elemento_por_indice(4)
print(f"No índice 4 está o elemento: {valor_no_indice_4}") # Saída: 40

# 5. Remova um elemento
removido = lista.remover_elemento(10)
if removido:
    print("Elemento 10 removido com sucesso!")

print(lista)
# Saída esperada: 0 => 20 => 30 => 40 => None
