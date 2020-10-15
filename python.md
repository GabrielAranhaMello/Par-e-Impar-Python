# Par-ou-imapar-com-o-Python
# Esse projeto é sobre um jogo em que você par ou ímpar e um número contra o bot e o programa ainda calcula quantas vezes você ganhou consecutivamente
import random
import time
cont = a = contTF = 0

while True:
    pí = int(input('Escolha ÍMPAR(1) ou PAR(2): '))
    num = int(input('Digite um número de 1 á 10: '))
    ranb = random.randint(1, 11)
    calc = ranb + num
    cont += 1

    if (num + ranb) % 2 == 0:
        parim = 'PAR'
    if (num + ranb) % 2 != 0:
        parim = 'ÍMPAR'
    print(f'O BOT escolheu {ranb}')
    print(f'{num} + {ranb} é igual á {num + ranb},um número {parim}')

    if pí == 2:
        bot = 1
    elif pí == 1:
        bot = 2

    if pí == 1 and calc % 2 != 0:

        TorF = True
        contTF += 1

        print('Calculando', end='')
        time.sleep(1)
        print('.', end='')
        time.sleep(1)
        print('.', end='')
        time.sleep(1)
        print('.')
        time.sleep(0.5)
        print('=' * 40)
        print(f'Você \033[4;33mganhou\033[m!!O BOT escolheu {ranb}')
        print('=' * 40)


    elif pí == 2 and calc % 2 == 0:

        TorF = True
        contTF +=1

        print('Calculando', end='')
        time.sleep(1)
        print('.', end='')
        time.sleep(1)
        print('.', end='')
        time.sleep(1)
        print('.')
        time.sleep(0.5)
        print('=' * 40)
        print(f'Você \033[4;33mganhou\033[m!!O BOT escolheu {ranb}')
        print('=' * 40)


    else:

        TorF = False

        print('Calculando', end='')
        time.sleep(1)
        print('.', end='')
        time.sleep(1)
        print('.', end='')
        time.sleep(1)
        print('.')
        time.sleep(0.5)
        print('=' * 40)
        print(f'Você \033[31;4mperdeu\033[m!!O BOT escolheu {ranb}')
        print('=' * 40)

        break


        if TorF == True:

            contTF += 1

            print('JOGUE DENOVO ATÉ PERDER!')
            time.sleep(2)
            pí = int(input('Escolha ÍMPAR(1) ou PAR(2): '))
            num = int(input('Digite um número de 1 á 10: '))
            ranb = random.randint(1, 11)
            calc = ranb + num

            if (num + ranb) % 2 == 0:
                parim = 'PAR'
            if (num + ranb) % 2 != 0:
                parim = 'ÍMPAR'
            print(f'O BOT escolheu {ranb}')
            print(f'{num} + {ranb} é igual á {num + ranb},um número {parim}')

            if pí == 2:
                bot = 1
            elif pí == 1:
                bot = 2

            if pí == 1 and calc % 2 != 0:

                contTF += 1

                print('Calculando', end='')
                time.sleep(1)
                print('.', end='')
                time.sleep(1)
                print('.', end='')
                time.sleep(1)
                print('.')
                time.sleep(0.5)
                print('=' * 40)
                print(f'Você \033[4;33mganhou\033[m!!O BOT escolheu {ranb}')
                print('=' * 40)


            elif pí == 2 and calc % 2 == 0:

                print('Calculando', end='')
                time.sleep(1)
                print('.', end='')
                time.sleep(1)
                print('.', end='')
                time.sleep(1)
                print('.')
                time.sleep(0.5)
                print('=' * 40)
                print(f'Você \033[4;33mganhou\033[m!!O BOT escolheu {ranb}')
                print('=' * 40)


            else:

                print('Calculando', end='')
                time.sleep(1)
                print('.', end='')
                time.sleep(1)
                print('.', end='')
                time.sleep(1)
                print('.')
                time.sleep(0.5)
                print('=' * 40)
                print(f'Você \033[31;4mperdeu\033[m!!O BOT escolheu {ranb}')
                print('=' * 40)

            if TorF == False:
                print('Você perdeu!!')
                break


if cont == 1:
    print('Você não ganhou nenhuma vez (-_-)')

elif cont == 2:
    print('Você ganhou uma vez!')

elif contTF >=\
        2:
    print(f'Você ganhou {contTF} vezes consecutivas!')
