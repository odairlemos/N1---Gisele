'''
Darth Vader achou que seu exército de stormtrooper estava prendendo poucos rebeldes, então lhe contratou para desenvolver
um programa que leia um conjunto indeterminado de números de refém preso por mês. Ao final da listagem informa o menor
 e maior número de capturados, a média e o valor mais próximo a média
'''
lista_refem=[]
refem_temp=0
max=0
min=999999
index=0
media=0
proximo=9999
aux=0
menu=True


while menu:
    op=int(input("1- adicionar numero de refens capiturados\n"
                 "2- lista geral de refens\n"
                 "3- o maior numero de refens capturados\n"
                 "4- o menor numero de refens capturados\n"
                 "5- media de refens capiturados\n"
                 "6- valor mais proximo a media\n"
                 "7- sair\n"
                 "opção:"))

    if op==1:
        refem_temp=int(input("digite o numero de refem capiturado: "))

        lista_refem.append(refem_temp)

        index=index+1


    elif op==2:
        print(lista_refem)


    elif op==3:
        for i in range(len(lista_refem)):

            if lista_refem[i]>max:

                max=lista_refem[i]
        print("o maior numero de refens capiturado é: ",max)


    elif op==4:
        for i in range(len(lista_refem)):

            if lista_refem[i] < min:

                min = lista_refem[i]
        print("o menor numero de refens capiturados é: ",min)


    elif op==5:
        for i in range(len(lista_refem)):

            media= media + lista_refem[i]

        media=media/index
        print("a media de refens é: {0:.2f}".format(media))


    elif op ==6:
        for i in range(len(lista_refem)):
            aux= lista_refem[i]/media

            if proximo>aux:
                proximo=lista_refem[i]

        print("o numero mais proximo da media é: ",proximo)

    elif op==7:
        menu=False