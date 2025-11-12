# szorg2.2

Cél:
A program az ASCII-art szövegfájlokat egyszerű, nyomtatható ASCII-karakterekre épülő algoritmussal tömöríti.  
A cél a fájlméret csökkentése a megadott szabályok betartásával.

Módszer

Tömörítés:
- A program soronként dolgozik (`tomorit_sor()` függvény).
- Az egymás után ismétlődő karaktereket rövidíti:  
  pl. `AAAAA` → `~A5`.
- 4-nél kevesebb ismétlés esetén nem történik tömörítés, mert nem éri meg.
- A `~` jel duplázással (`~~`) kerül kódolásra, hogy egyértelmű maradjon.

Kitömörítés:
- A `kitomorit_sor()` függvény a `~A5` alakú szekvenciákat visszaalakítja `AAAAA` formára.
- Nem használ memóriát vagy korábbi sorokat, minden sort önállóan kezel.

Fájlkezelés:
- Az összes `.txt` fájlt feldolgozza a megadott könyvtárban.
- Az eredmény `_ascii.txt` kiterjesztéssel mentésre kerül.
- A program minden fájlra kiírja:
  - az eredeti méretet,  
  - a tömörített méretet,  
  - és a tömörítési arányt százalékban.

Kimenet formátuma:
név, eredeti méret, tömörített méret, tömörítési arány %
kave.txt, 262, 164, 62.6%
kutya.txt, 300, 257, 85.7%
madar.txt, 34, 32, 94.1%
nlabda.txt, 2102, 982, 46.7%

