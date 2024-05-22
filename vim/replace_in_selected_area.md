# --VISUAL. Shift + :

Vim knowledge boom moment: I saw how ThePrimeagen did "add lost brackets to the end of the line for this N lines".

It works this way:
- select the lines (in --VISUAL mode)
- press `shift+:`
- it shows `:'<'>` and here I can use any of commands.

For this example it was 
```
:s/%pattern_to_change%$/%new_pattern/g
```
Dollar sign is the sign "The end of the line"
