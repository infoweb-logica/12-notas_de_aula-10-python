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
Resumo da [parte 1](/11-funções-parte_1.pdf)
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

Resumo da [parte 2](/11-funções-parte_2.pdf)
1. FIXME

---
## Exercícios [Lista de exercícios](/lista.md)
**Parte 1**
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


**Parte 2**
1. FIXME
