# Estudo de Bibliotecas - Random

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
