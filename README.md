# calcular_media.py
def calcular_media(numeros):
    if len(numeros) == 0:
        return 0
    return sum(numeros) / len(numeros)

def main():
    print("Este programa calcula a média de uma lista de números.")
    numeros = []

    while True:
        entrada = input("Digite um número (ou 'done' para terminar): ")
        if entrada.lower() == 'done':
            break
        try:
            numero = float(entrada)
            numeros.append(numero)
        except ValueError:
            print("Por favor, insira um número válido.")

    media = calcular_media(numeros)
    print("A média dos números é:", media)

if __name__ == "__main__":
    main()
