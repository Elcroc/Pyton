''' code fibonacci questão 2 '''

num = int(input("Digite um número: "))
fib1 = 0
fib2 = 1
fib = 0

while fib < num:
    fib = fib1 + fib2
    fib1 = fib2
    fib2 = fib

if fib == num:
    print(f"O número {num} pertence à sequência de Fibonacci.")
else:
    print(f"O número {num} não pertence à sequência de Fibonacci.")
    
''' code vetor + json questão 3 '''    
 import json

with open('faturamento.json', 'r') as file:
    faturamento = json.load(file)
menor_valor = min(faturamento.values())

maior_valor = max(faturamento.values())

valores = [valor for valor in faturamento.values() if valor > 0]
media = sum(valores) / len(valores)

dias_acima_da_media = len([valor for valor in valores if valor > media])

print(f"Menor valor de faturamento: R$ {menor_valor:.2f}")
print(f"Maior valor de faturamento: R$ {maior_valor:.2f}")
print(f"Número de dias acima da média: {dias_acima_da_media}")

''' code faturamento questão 4 '''


faturamento = {'SP': 67836.43, 'RJ': 36678.66, 'MG': 29229.88, 'ES': 27165.48, 'Outros': 19849.53}

total = sum(faturamento.values())

percentuais = {estado: (valor / total) * 100 for estado, valor in faturamento.items()}

for estado, percentual in percentuais.items():
    print(f"{estado}: {percentual:.2f}%")

''' code Iverter questão 5'''
    
def inverter_string(s):
   
    lista = list(s)   
    tamanho = len(lista)

    esquerda = 0
    direita = tamanho - 1
    while esquerda < direita:      
        lista[esquerda], lista[direita] = lista[direita], lista[esquerda]
        esquerda += 1
        direita -= 1    
    return ''.join(lista)
