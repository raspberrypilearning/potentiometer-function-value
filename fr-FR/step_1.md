Si tu utilises un potentiomètre pour contrôler les sorties, tu devras diviser le cadran en sections égales.

Tu peux utiliser `dial.value` pour obtenir une valeur entre 0 et 1 du potentiomètre.

**Astuce :** Tu peux multiplier la valeur par 100 pour obtenir un pourcentage. Si tu as cinq humeurs, tu peux vérifier si la valeur est inférieure à 20, 40, 60, 80 ou 100. Si tu as trois humeurs, tu peux vérifier si la valeur est inférieure à 33, 66 ou 100.

--- code ---
---
language: python 
filename: sensory-gadget.py 
line_numbers: false 
line_number_start:
line_highlights:
---

while True:
    humeur = dial.value * 100 # convertir en pourcentage
    print(humeur)
    if humeur < 20:
        heureux()
    elif humeur < 40:
        bien()
    elif humeur < 60:
        ok()
    elif humeur < 80:
        incertain()
    else:
        malheureux()
    sleep(0.1) 

--- /code ---
