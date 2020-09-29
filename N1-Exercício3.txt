nota = -1

while nota < 0 or nota > 10:
    nota = int(input("Informe a nota: "))

    if nota < 0 or nota > 10:
        print("Valor inválido")