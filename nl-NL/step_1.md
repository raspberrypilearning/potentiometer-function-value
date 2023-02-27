Als je een potentiometer gebruikt om uitvoer te regelen, dan moet je het instelwiel in gelijke secties verdelen.

Je kunt `dial.value` gebruiken om een waarde tussen 0 en 1 van de potentiometer te krijgen.

**Tip:** Je kunt de waarde met 100 vermenigvuldigen om een percentage te krijgen. Als je vijf stemmingen hebt, kun je controleren of de waarde lager is dan 20, 40, 60, 80 of 100. Als je drie stemmingen hebt, kun je controleren of de waarde minder is dan 33, 66 of 100.

--- code ---
---
language: python filename: sensory-gadget.py line_numbers: false line_number_start:
line_highlights:
---

while True: mood = dial.value * 100 # turn to a percentage print(mood) if mood < 20: happy() elif mood < 40: good() elif mood < 60: okay() elif mood < 80: unsure() else: unhappy() sleep(0.1)

--- /code ---
