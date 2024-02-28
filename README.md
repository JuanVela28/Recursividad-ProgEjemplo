# Recursividad-ProgEjemplo

class Nodo:
    def __init__(self, valor):
        self.valor = valor
        self.izquierda = None
        self.derecha = None

class ArbolBinario:
    def __init__(self, raiz):
        self.raiz = raiz

    def suma_nodos(self, nodo):
        if nodo is None:
            return 0
        else:
            return nodo.valor + self.suma_nodos(nodo.izquierda) + self.suma_nodos(nodo.derecha)

nodo1 = Nodo(1)
nodo2 = Nodo(2)
nodo3 = Nodo(3)
nodo4 = Nodo(4)
nodo5 = Nodo(5)
nodo6 = Nodo(6)

nodo1.izquierda = nodo2
nodo1.derecha = nodo3
nodo2.izquierda = nodo4
nodo2.derecha = nodo5
nodo3.derecha = nodo6

arbol = ArbolBinario(nodo1)

suma_total = arbol.suma_nodos(arbol.raiz)
print("La suma de todos los nodos en el árbol es:", suma_total)
