# Exercícios — Funções em Python

> **Público alvo**: alunos da disciplina de Introdução a Lógica e Programação  
> **Objetivo**: criar funções para resolver problemas de programação  

---

## Parte 1

1. Escreva uma função com três parâmetros inteiros e que retorna a soma destes parâmetros. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 2<br />3<br />1                   | 6                |
| 0<br />5<br />2                   | 7                |

2. Escreva uma função com dois parâmetros inteiros e que retorna a multiplicação destes parâmetros. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 2<br />3                          | 6                |
| 0<br />5                          | 0                |

3. Escreva uma função que recebe um inteiro como parâmetro e que imprime uma mensagem indicando se o inteiro é par ou ímpar. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Impressão esperada |
| --------------------------------- | ------------------ |
| 2                                 | Par                |
| 5                                 | Ímpar              |
| 0                                 | Par                |

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

6. Escreva uma função que recebe um inteiro n ≥ 0 como parâmetro e que retorna a soma dos inteiros de 1 a n. Escreva pelo menos três testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 3                                 | 6                |
| 10                                | 55               |
| 1                                 | 1                |
| 0                                 | 0                |

7. Escreva uma função que recebe dois números reais, base e altura, e retorna a área de um triângulo. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 6.0<br />4.0                      | 12.0             |
| 3.0<br />5.0                      | 7.5              |

8. Escreva uma função que recebe um número real em graus Celsius e retorna o equivalente em Fahrenheit. A fórmula de conversão é: `F = C * 9/5 + 32`. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 0                                 | 32.0             |
| 100                               | 212.0            |
| 37                                | 98.6             |

9. Escreva uma função que recebe quatro números reais e retorna a média aritmética deles. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros      | Retorno esperado |
| -------------------------------------- | ---------------- |
| 6.0<br />7.0<br />8.0<br />9.0         | 7.5              |
| 10.0<br />10.0<br />10.0<br />10.0     | 10.0             |
| 0.0<br />5.0<br />3.0<br />8.0         | 4.0              |

10. Escreva uma função que recebe um inteiro positivo e retorna a soma de seus algarismos. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 123                               | 6                |
| 9                                 | 9                |
| 405                               | 9                |

---

## Parte 2

11. Escreva uma função que recebe um inteiro n > 1 e retorna `True` se n for primo ou `False` caso contrário. Escreva pelo menos três testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 2                                 | True             |
| 7                                 | True             |
| 9                                 | False            |
| 13                                | True             |

12. Escreva uma função que recebe um inteiro n ≥ 0 e retorna o fatorial de n. Lembre que 0! = 1. Escreva pelo menos três testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 0                                 | 1                |
| 1                                 | 1                |
| 5                                 | 120              |
| 6                                 | 720              |

13. Escreva uma função que recebe uma string e retorna a mesma string invertida. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| Python                            | nohtyP           |
| abcd                              | dcba             |
| a                                 | a                |

14. Escreva uma função que recebe uma string e retorna `True` se ela for um palíndromo (lida da mesma forma de trás para frente), ou `False` caso contrário. Ignore maiúsculas e minúsculas. Escreva pelo menos três testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| ama                               | True             |
| arara                             | True             |
| Python                            | False            |
| Ovo                               | True             |

15. Escreva uma função que recebe uma string e retorna a quantidade de vogais presentes nela. Considere as vogais: a, e, i, o, u (maiúsculas e minúsculas). Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| Python                            | 1                |
| Banana                            | 3                |
| AEIOU                             | 5                |
| Xyz                               | 0                |

16. Escreva uma função que recebe um ano inteiro e retorna `True` se for bissexto ou `False` caso contrário. Um ano é bissexto se for divisível por 4, exceto anos centenários, que só são bissextos se também forem divisíveis por 400. Escreva pelo menos três testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 2000                              | True             |
| 1900                              | False            |
| 2024                              | True             |
| 2023                              | False            |

17. Escreva uma função que recebe dois inteiros, dividendo e divisor, e retorna o quociente e o resto da divisão inteira. Escreva pelo menos dois testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 10<br />3                         | 3<br />1         |
| 20<br />4                         | 5<br />0         |
| 7<br />2                          | 3<br />1         |

18. Escreva uma função que recebe um número inteiro e retorna o seu valor absoluto sem usar a função embutida `abs()`. Escreva pelo menos três testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| -5                                | 5                |
| 3                                 | 3                |
| 0                                 | 0                |

19. Escreva uma função que recebe um inteiro n ≥ 0 e retorna o n-ésimo número da sequência de Fibonacci. Considere que F(0) = 0 e F(1) = 1. Escreva pelo menos quatro testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 0                                 | 0                |
| 1                                 | 1                |
| 6                                 | 8                |
| 10                                | 55               |

20. Escreva uma função que recebe três números reais representando os lados de um triângulo e retorna `'Equilátero'`, `'Isósceles'` ou `'Escaleno'` conforme o tipo do triângulo. Escreva pelo menos três testes da função no programa principal.

| Exemplos de valores de parâmetros | Retorno esperado |
| --------------------------------- | ---------------- |
| 3.0<br />3.0<br />3.0             | Equilátero       |
| 4.0<br />4.0<br />6.0             | Isósceles        |
| 3.0<br />4.0<br />5.0             | Escaleno         |

---

## Parte 3

21. Qual é a saída do programa Python a seguir?

```python
def delta(a, b, c):
  delta = b ** 2 - 4 * a * c
  return delta

print(delta(10, 5, 0))
print(delta(1, 0, 1))
```

22. Qual é a saída do programa Python a seguir?

```python
def impressao(s, c, n):
  return c * n + s + c * n

print(impressao('PAULA', '*', 4))
print(impressao('João Pedro', '-', 6))
```

23. Qual é a saída do programa Python a seguir?

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

24. Qual é a saída do programa Python a seguir?

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

25. Qual é a saída do programa Python a seguir?

```python
def classifica(n):
  if n < 0:
    return 'negativo'
  elif n == 0:
    return 'zero'
  elif n % 2 == 0:
    return 'positivo par'
  else:
    return 'positivo ímpar'

valores = [-3, 0, 4, 7, -10, 2]
for v in valores:
  print(v, '->', classifica(v))
```
