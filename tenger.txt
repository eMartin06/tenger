# Írjon programot tengerszint néven!
# Kérjen be addig földrajzi hely nevét és tengerszint feletti magasságát, 
# amíg üres karaktert nem üt a felhasználó!

# Írjon függvényt!
# a tengerszintek néven, amely alföldet,"dombságot,"középhegység" és "magashegység" különböztet meg!
# 200m alatt alföldet,
# 200m és 500m között dombságot
# 500m és 1500m között középhegység
# 1500m magashegység


# # Fájl írása tenger.txt néven az amelyben az összes eredmény szerepel!

# Beadandó

# A program forráskódja .py kiterjesztéssel a Githubra!
# A program forráskódja .txt kiterjesztéssel dkt-ra!

wr=open('H:\tenger.txt','w')

def tengerszint2(tengersz):
    if tengersz < 200:
        return("Alfold")
    elif tengersz >200 and 500:
        return("Dombság")
    elif tengersz >500 and 1500:
        return("Hegység")
    else:
        return("Magashegység")

földrajzinev=input('Adjon meg egy földrajzi hely nevét! ')
wr.write('Adjon meg egy földrajzi hely nevét!\n')
tengersz=int(input('Adja meg a földrajzi helynek a magasságát méterben! '))
wr.write('Adja meg a földrajzi helynek a magasságát méterben!\n')


while földrajzinev =="" and tengersz =="":
    if földrajzinev =="" and tengersz =="":
        földrajzinev=input('Adjon meg egy földrajzi hely nevét!  ')
        tengersz=input('Adja meg a földrajzi helynek a magasságát méterben! ')
        tengersz=int(tengersz)
        
print(f'A {földrajzinev} az {tengersz} méter és egy {tengerszint2(tengersz)}')
wr.write(f'A {földrajzinev} az {tengersz} méter és egy {tengerszint2(tengersz)}\n')

wr.close()
