# Notas de aula de 2026.1.10 - Python Funções

## Informações gerais

- **Público alvo**: alunos da disciplina de **Introdução a lógica e programação** do curso de [Infoweb](https://diatinf.ifrn.edu.br/cursos/tecnico-em-informatica-para-internet/) na [DIATINF](https://diatinf.ifrn.edu.br/) no [CNAT-IFRN](https://portal.ifrn.edu.br/campus/natalcentral/)
- **Professor**: [L A Minora](https://github.com/leonardo-minora/)
- **Objetivo**:
  1. Apresentar o conceito de funções na programação
  2. Apresentar a anatomia de uma função
  2. Mostrar como criar funções

---
## Notas de aula

### Resumo da [parte 1](/11-funções-parte_1.pdf)
1. **Funções**: uma função define um bloco de código que pode ser reutilizado por programas
2. **Chamada de função**: momento que uma função está sendo **utilizada**
3. **Anatomia de uma função**: foco na chamada de função
   - **identificador**: identificado por um nome e um par de parênteses
   - **parâmetros** ou argumentos: são os valores ou variáveis presentes dentro do seu par de parênteses
4. **Definir uma função**:
   - Programadores podem criar suas próprias funções através da instrução `def`. 
   - Funções devem ser definidas antes do programa principal.
   - Código presente no  corpo de uma função é executado apenas quando a função é chamada.
5. **Anatomia de uma função**: foco na definição de uma função
   - **def**: palavra reservada do python para definir uma função. deve ser colocada antes do nome identificador
   - **identificador**: identificado por um nome e um par de parênteses
   - **parâmetros** ou argumentos: são os valores ou variáveis presentes dentro do seu par de parênteses
   - **valor de retorno** ou de resultado:
     1. função retorne um valor para o programa principal ao invés de realizar uma impressão.
     2. O retorno de um valor é feito com a instrução return.

### Resumo da [parte 2](/11-funções-parte_2.pdf)
1. Escopo de variáveis
   - **locais**: 
      - São as variáveis definidas no corpo de uma função e os seus parâmetros.
      - Variáveis locais são visíveis apenas no próprio corpo da função.
      - O valor de uma variável local é reinicializado toda vez que a função é chamada.
   - **globais**: 
      - São as variáveis definidas no programa principal.
      - Variáveis globais são visíveis para o programa principal bem como para as funções.
      - **EVITE USAR** porque aumenta a probabilidade de ocorrência de bugs em programas.
2. Funções
   - definição da função
     - Instrução `global`: permite que uma variável dentro da função acesse a variável com escopo `global`
     - Instrução `return`: permite que a função seja encerrada e retorne valores para o chamador
     - Parâmetros opcionais: são parâmetros cujo valor não precisa ser informado no momento em que uma função é chamada.
   - chamada da função
     - chamada com parâmetro nomeados: 
       - ao chamar uma função podemos informar os valores dos parâmetros em conjunto, ou não, dos nomes dos parâmetros
       - parâmetros obrigatórios podem ter seus nomes omitidos, mas nesse caso deve-se seguir a ordem de definição dos parâmetros obrigatórios.

### Exemplos de códigos python

Acessar variáveis locais fora da função.
```python
def soma(a, b):
  s = a + b
  return s

x, y = 5, 8
sm = soma(x, y)
print(sm)
print(a) # gera erro
print(b) # gera erro
print(s) # gera erro
``` 

Acessar variável global dentro de uma função. **EVITE**
```python
def soma(a):
  return x + a

x = 5
y = soma(11)
print(y) # 16
```

Variável local e global com o mesmo identificador (nome).
```python
def soma(a, b):
  s = a + b
  return s

a, b, s = 5, 8, 0
sm = soma(11, 4)
print(sm) # 15
print(a)  # 5
print(b)  # 8
print(s)  # 0
```

Uso da instrução `gloval`. **EVITE**
```python
def muda_x():
  global x
  x = "Bola"

x = "Casa"
print(x)  # Casa
muda_x()
print(x)  # Bola
```

Uso da instrução `return`.
```python
def avaliar(x):
  if x == 1:
    return 1
  return 0

print(avaliar(1))
print(avaliar(3))
```

Definição de parâmetros opcioniais.
```python
def linha(n, caractere='*'):
  print(caractere * n)

linha(10)
linha(15, '-')
linha()      	 # gera erro
```
`
Chamada com parâmetros nomeados.
```python
def a_divisivel_por_b(a, b):
  print(a % b == 0)

a_divisivel_por_b(10, 2) 	    # True
a_divisivel_por_b(2, 10) 	    # False
a_divisivel_por_b(a=20, b=5)    # True
a_divisivel_por_b(b=3, a=15)    # True
a_divisivel_por_b(2, b=10)      # False
a_divisivel_por_b(b=3, 15)      # Gera erro
a_divisivel_por_b(2, a=3)       # Gera erro
a_divisivel_por_b(2, a=3, b=5)  # Gera erro
```

```python
def a_divisivel_por_b(a, b, adorno=''):
  print(adorno, a % b == 0, adorno)

a_divisivel_por_b(10, 2)                  # True
a_divisivel_por_b(2, 10) 	              # False
a_divisivel_por_b(2, 10, '*'	)             # False
a_divisivel_por_b(10, 2, adorno='*')      # * True *
a_divisivel_por_b(2, 10, adorno='*')      # * False *
a_divisivel_por_b(b=5, a=20)              # True
a_divisivel_por_b(a=15, b=3, adorno='*')  # * True *
a_divisivel_por_b(10, adorno='*', b=5)    # * True *
a_divisivel_por_b(a=10, 2) 	              # Gera erro
```

---
## Exercícios [Lista de exercícios](/lista.md)
### **Parte 1**
1. Escreva uma função com três parâmetros inteiros e que retorna a soma destes parâmetros. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 2<br />3<br />1                   | 6                |
| 0<br />5<br />2                   | 7                |

**Solução**
```python
def soma(a, b, c):
  return a + b + c

# teste 1
s = soma(2, 3, 1)
print('2 + 3 + 1 =', s)

# teste 2
s = soma(0, 5, 2)
print('0 + 5 + 2 =', s)

```` 
2. Escreva uma função com dois parâmetros inteiros e que retorna a multiplicação destes parâmetros. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 2<br />3                          | 6                |
| 0<br />5                          | 0                |

3. Escreva uma função que recebe um inteiro como parâmetro e que imprime uma mensagem indicando se o inteiro é par ou ímpar. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 2                                 | Par              |
| 5                                 | Ímpar            |
| 0                                 | Par              |

4. Escreva uma função com cinco parâmetros inteiros e que retorna, nessa ordem, o menor e maior valores fornecidos como parâmetros. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 2<br />10<br />5<br />0<br />-4   | -4<br />10       |
| 5<br />2<br />2<br />-10<br />5   | -10<br />5       |

5. Escreva uma função que recebe uma palavra P e uma letra L como parâmetros e que retorna a quantidade de ocorrências de L em P. Escreva pelo menos três testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| Banana<br />a                     | 3                |
| CASA<br />s                       | 0                |
| Caju<br />b                       | 0                |

6. Escreva uma função que recebe um inteiro n > 0 como parâmetro e que retorna a soma dos inteiros de 1 a n. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 3                                 | 6                |
| 10                                | 55               |
| 1                                 | 1                |
| 0                                 | 0                |

7. Qual é saída do programa Python a seguir?

```python
def delta(a, b, c):
  delta = b ** 2 - 4 * a * c
  return delta

print(delta(10, 5, 0))
print(delta(1, 0, 1))

``` 

8. Qual é saída do programa Python a seguir?

```python
def impressao(s, c, n):
  return c * n + s + c * n

print(impressao('PAULA', '*', 4))
print(impressao('João Pedro', '-', 6))

``` 

9. Qual é saída do programa Python a seguir?

```python
def raiz(a, b):
  if a == 0:
    return None
  return - b / a

print(raiz(4, 12))
print(raiz(5, 0))
print(raiz(0, -3))
print(raiz(-2, 5))

``` 

10. Qual é saída do programa Python a seguir?

```python
def sequencia(a, b):
  if b % 2 == 0:
    for i in range(2, a * 2 + 1, 2):
      print(i, end=' ')
  else:
    for i in range(1, a * 2 + 1, 2):
      print(i, end=' ')
  print('')

sequencia(5, 2)
sequencia(5, 1)
sequencia(4, 3)
sequencia(3, 4)

``` 

---

### **Parte 2**
1. Qual é saída do programa Python a seguir?
```python
def funcao(a):
   b = a * 2 + 1
   return b

b = 10
a = funcao(b)
print(a)
print(b)

```

2. Qual é saída do programa Python a seguir?
```python
def funcao(x):
   if x == 0:
      x = 1
   y = 5 / x
   return y

x = 5
y = funcao(x)
print(x)
print(y)
y = -5
funcao(y)
print(x)
print(y)

```

3. Qual é saída do programa Python a seguir?

```python
def funcao(y):
   if y < 0:
      x = 1
      return y
   return y + 2

x = 0
w = funcao(10)
print(x)
print(w)
w = funcao(-3)
print(x)
print(w)

```

4. Qual é saída do programa Python a seguir?

```python
def funcao(y):
   global x
   if y < 0:
      x = 1
      return y
   return y + 2

x = 0
w = funcao(10)
print(x)
print(w)
w = funcao(-3)
print(x)
print(w)

```

5. Qual é saída do programa Python a seguir?

```python
def funcao(i):
   if -3 < i < -1:
      return 'Z'
   elif i == 0:
      return 'Y'
   x = i % 3
   if x == 0:
      return 'T'
   elif x == 1:
      return 'U'
   return 'W'

print(funcao(3))
print(funcao(5))
print(funcao(0))
print(funcao(4))
print(funcao(-10))
print(funcao(-2))

```

6. Considerando as chamadas a seguir e a implementação apresentada no quadro, indique o valor de retorno da chamada de função ou se a chamada gera um erro.
   1. `funcao(1, 2)`
   2. `funcao(1, 2, 6)`
   3. `funcao(10)`
   4. `funcao(3, 2, d=10)`
   5. `funcao(3, 2, d=10, c=0)`
   6. `funcao(d=10, c=0, 2, 1)`
   7. `funcao(a=10, 0, 2, 1)`
   8. `funcao(a=10, d=3, c=1, b=5)`
   9. `funcao(5, b=3, d=1, c=2)`

```python
def funcao(a, b, c=3, d=0):
   return a + b + c + d

```