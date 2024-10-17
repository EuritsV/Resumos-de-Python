# Resumos-de-Python


1. Tipos de dados em Python
Python possui vários tipos de dados integrados, como:

int: Números inteiros (ex: 1, -2, 0)
float: Números de ponto flutuante (ex: 1.5, -0.5)
str: Cadeia de caracteres ou strings (ex: "Olá", "Python")
bool: Valores booleanos (True, False)
Exemplo:
a = 10          # int
b = 3.14        # float
c = "Python"    # str
d = True        # bool
2. Listas
Listas são coleções ordenadas e mutáveis de itens. Elas podem conter diferentes tipos de dados.

Exemplo:

lista = [1, 2, 3, "Python", 3.14]
print(lista)
Operações com listas:

lista.append(4)        # Adicionar elemento
lista[0] = 100         # Alterar elemento
print(lista[1:3])      # Fatiamento (sublista)
3. Operadores
Python suporta vários tipos de operadores:

Aritméticos: +, -, *, /, // (divisão inteira), % (módulo), ** (exponenciação)
Comparação: ==, !=, >, <, >=, <=
Lógicos: and, or, not
Exemplo:

x = 10
y = 3
resultado = x ** y  # Exponenciação: 10^3 = 1000
print(resultado)
4. Funções
Funções são blocos de código que executam uma tarefa específica. Você pode criar suas próprias funções usando def.

Exemplo:

def soma(a, b):
    return a + b

resultado = soma(10, 5)
print(resultado)  # Saída: 15
5. Arrays
Python não tem um tipo array nativo como algumas outras linguagens, mas o módulo array pode ser usado para trabalhar com arrays.

Exemplo:

import array as arr

meu_array = arr.array('i', [1, 2, 3, 4, 5])  # 'i' representa inteiros
print(meu_array)
6. Classes e Objetos
Classes são a base da programação orientada a objetos (OOP) em Python. Objetos são instâncias de classes.

Exemplo de criação de uma classe:

class Pessoa:
    def __init__(self, nome, idade):  # Construtor
        self.nome = nome
        self.idade = idade

    def saudacao(self):
        return f"Olá, meu nome é {self.nome} e tenho {self.idade} anos."

pessoa1 = Pessoa("João", 25)
print(pessoa1.saudacao())
7. Construtores
O método __init__ é o construtor em Python. Ele é chamado automaticamente quando uma nova instância da classe é criada.

Exemplo:

class Carro:
    def __init__(self, marca, modelo):
        self.marca = marca
        self.modelo = modelo

meu_carro = Carro("Toyota", "Corolla")
print(meu_carro.marca)
8. Polimorfismo
Polimorfismo permite que diferentes classes tenham métodos com o mesmo nome, mas com comportamentos diferentes.

Exemplo:

class Ave:
    def som(self):
        print("Piu piu")

class Cachorro:
    def som(self):
        print("Au au")

animais = [Ave(), Cachorro()]

for animal in animais:
    animal.som()
9. Dicionários
Dicionários são coleções não ordenadas de pares chave: valor. Você pode usar uma chave para acessar o valor correspondente.

Exemplo:

meu_dicionario = {
    "nome": "Alice",
    "idade": 30,
    "cidade": "São Paulo"
}
print(meu_dicionario["nome"])  # Saída: Alice
10. Estruturas Condicionais: if
A instrução if permite executar um bloco de código com base em uma condição.

Exemplo:

idade = 18
if idade >= 18:
    print("Maior de idade")
else:
    print("Menor de idade")
11. Loops: for e while
For: Utilizado para percorrer itens em uma lista ou range.
Exemplo:

for i in range(5):  # Itera de 0 a 4
    print(i)
While: Executa um bloco de código enquanto a condição é verdadeira.
Exemplo:

x = 0
while x < 5:
    print(x)
    x += 1
Resumo Completo:
Aqui está um exemplo que integra muitos dos conceitos anteriores:

# Classe que representa uma pessoa
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def saudacao(self):
        return f"Olá, meu nome é {self.nome}"

# Função para verificar se a pessoa é maior de idade
def verificar_maioridade(pessoa):
    if pessoa.idade >= 18:
        return True
    else:
        return False

# Lista de objetos Pessoa
pessoas = [Pessoa("João", 20), Pessoa("Maria", 17), Pessoa("Ana", 30)]

# Loop para verificar maioridade
for pessoa in pessoas:
    if verificar_maioridade(pessoa):
        print(f"{pessoa.nome} é maior de idade.")
    else:
        print(f"{pessoa.nome} é menor de idade.")
