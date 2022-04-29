def provGorodov(vnutrSpisok,VvodGoroda):
    global proverka
    for z in vnutrSpisok:
        if z == VvodGoroda:
            proverka = 1
            ispGoroda.append(z)
            break
        elif VvodGoroda != i:
            proverka = 0
            continue
        else:
            break
    return(ispGoroda,proverka)

def provNaPovtor(ispGoroda,VvodGoroda):
    global Povtor
    for i in ispGoroda:
        if i == VvodGoroda:
            Povtor = 0
            break
        elif i!=VvodGoroda:
            Povtor = 1
            continue
    return(Povtor)

def proverkaNaPravila(VvodGoroda,lastBukva):
    global k
    if VvodGoroda[0]==lastBukva:
        k=1
    elif VvodGoroda[0]!=lastBukva:
        k=0
    return(k)

def proverkaNaEnter():
    global VvodGoroda
    while len(VvodGoroda)==0:
        if len(VvodGoroda)==0:
            print('Введите название города:')
            VvodGoroda = str(input().lower())
        elif len(VvodGoroda)>=1:
            continue
    return(VvodGoroda)

def proverkaNaZnakiIprobel():
    global pervayaBukva
    while True:
        if pervayaBukva != 'а' and 'б' and'в'and'г' and'д' and 'е' and'ё'and'ж' and'з' and'и' and 'й' and 'к' and 'л' and'м' and'н'and'о'and'п'and'р'and'с'and'т'and'у'and'ф'and'х'and'ц'and'ч'and'ш'and'щ'and'ы'and'э'and'ю'and'я':
            print('Введите одну букву, без:', pervayaBukva)
            pervayaBukva = str(input().lower())
        else:
            break
    return(pervayaBukva)




print('Введите букву для первого города:')
pervayaBukva=str(input().lower())
VvodGoroda=str()
proverka=int()
ispGoroda=list()
lastBukva=str()
Povtor=1
K=0
z=0
proverkaNaZnakiIprobel()
while len(pervayaBukva)==1:
    if len(pervayaBukva)==1:
        vnutrSpisok=[pervayaBukva*2]
        lastBukva=pervayaBukva
        ispGoroda=[pervayaBukva]
        print(ispGoroda)
        break
    else:
        print('введите одну букву')
        pervayaBukva=str(input().lower())
        vnutrSpisok = [pervayaBukva * 2]
with open('SpisokGorodov.txt') as file:
    for i in file:
        vnutrSpisok.append(i.strip().lower())
print('Введите название города на:',pervayaBukva)
while VvodGoroda!='завершить':
    VvodGoroda=str(input().lower())
    proverkaNaEnter()
    provNaPovtor(ispGoroda,VvodGoroda)
    proverkaNaPravila(VvodGoroda,lastBukva)
    if k==1:
        if Povtor==0:
            proverka=2
        elif Povtor == 1:
            provGorodov(vnutrSpisok,VvodGoroda)
    elif k==0:
        proverka=3
    print(ispGoroda)
    poslBukva=ispGoroda[-1]
    if poslBukva[-1]== 'ь' and 'ъ':
        lastBukva = poslBukva[-2]
    else:
        lastBukva=poslBukva[-1]
    if proverka == 1:
        print('Отлично!, введите город на букву:', lastBukva)
    elif proverka==0:
        print('Такого города нет, введите город на:', lastBukva)
    elif proverka==2:
        print('Данный город уже был, введите город на:', lastBukva)
    elif proverka==3:
        print('Данный город не начинается на:',lastBukva,'Введите город на букву:',lastBukva)
    proverka=1
    Povtor=1
