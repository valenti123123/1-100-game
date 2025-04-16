import random

print("Bine ai venit la jocul 'Ghicește numărul'!")
print("Am ales un număr între 1 și 100. Încearcă să-l ghicești!")

# Generăm un număr aleatoriu între 1 și 100
numar_secret = random.randint(1, 100)
incercari = 0
ghicit = False

while not ghicit:
    # Solicităm utilizatorului să introducă un număr
    incercare = input("Introdu un număr: ")
    
    # Verificăm dacă utilizatorul a introdus un număr valid
    if not incercare.isdigit():
        print("Te rog să introduci un număr valid!")
        continue

    incercare = int(incercare)
    incercari += 1

    # Verificăm dacă numărul este corect
    if incercare < numar_secret:
        print("Prea mic! Încearcă din nou.")
    elif incercare > numar_secret:
        print("Prea mare! Încearcă din nou.")
    else:
        print(f"Felicitări! Ai ghicit numărul {numar_secret} în {incercari} încercări!")
        ghicit = True
