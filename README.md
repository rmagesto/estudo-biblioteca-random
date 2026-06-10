# Estudo de Bibliotecas - Random

Documentação oficial: https://docs.python.org/3/library/random.html

```python
import random

numeros = []

print("Digite 6 números entre 1 e 60")

while len(numeros) < 6:
    n = int(input("Número: "))

    if n < 1 or n > 60:
        print("Número inválido")
    elif n in numeros:
        print("Número repetido")
    else:
        numeros.append(n)

sorteio = random.sample(range(1, 61), 6)

numeros.sort()
sorteio.sort()

acertos = 0

for numero in numeros:
    if numero in sorteio:
        acertos += 1

print("\nSeus números:", numeros)
print("Números sorteados:", sorteio)
print("Você acertou", acertos, "número(s).")

if acertos == 6:
    print("Sena")
elif acertos == 5:
    print("Quina")
elif acertos == 4:
    print("Quadra")
```

Este exemplo usa a biblioteca `random` para simular um sorteio de seis números entre 1 e 60.

- O usuário informa seis números únicos dentro do intervalo.
- O programa valida se cada número está entre 1 e 60 e se não foi repetido.
- Em seguida, o sorteio escolhe seis números aleatórios diferentes com `random.sample`.
- Os dois conjuntos de números são ordenados e comparados para contar quantos acertos houve.
- Por fim, o programa exibe os números do usuário, os sorteados e a quantidade de acertos, além de imprimir `Sena`, `Quina` ou `Quadra` quando houver 6, 5 ou 4 acertos.

## Referências

[Estudo de bibliotecas](https://github.com/orlandosaraivajr/FATEC_1SEM26_LP2/issues/6)
