If you are using a potentiometer to control outputs, then you will need to divide up the dial into equal sections. 

You can use `dial.value` to get a value between 0 and 1 from the potentiometer. 

**Tip:** You can multiply the value by 100 to get a percentage. If you have five moods, then you can check whether the value is less than 20, 40, 60, 80, or 100. If you have three moods, then you can check whether the value is less than 33, 66, or 100. 

--- code ---
---
language: python
filename: sensory-gadget.py
line_numbers: false
line_number_start: 
line_highlights: 
---

while True:
    mood = dial.value * 100 # turn to a percentage
    print(mood)
    if mood < 20:
        happy()
    elif mood < 40:
        good()
    elif mood < 60:
        okay()
    elif mood < 80:
        unsure()
    else:
        unhappy()
    sleep(0.1) 

--- /code ---
