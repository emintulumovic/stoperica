# Štoperica

Projekat urađen u Flowcode-u. Simulira digitalnu štopericu koja mjeri proteklo vrijeme i prikazuje ga na LCD ekranu pomoću PIC mikrokontrolera.

## Kako radi

Osnova projekta je petlja koja se stalno izvršava i broji stotinke. Kad se nakupi 100 stotinki, sekunde se povećaju za jedan i stotinke se resetuju. Na isti način, kad sekunde dođu do 60, povećaju se minute. Rezultat se u svakom koraku ispisuje na LCD u formatu MM:SS:ss.

Program čita stanje tastera na svakom prolasku kroz petlju. U zavisnosti od toga koji je taster pritisnut, program ili nastavlja mjerenje, staje, bilježi međuvrijeme ili resetuje sve na početak:

| Taster | Funkcija |
|--------|----------|
| Start | Počinje mjerenje vremena |
| Stop | Pauzira mjerenje, ostaje na trenutnoj vrijednosti |
| Lap | Sprema trenutno međuvrijeme u posebne varijable |
| Reset | Postavlja minute, sekunde i stotinke na nulu |

## Tehnologije

- Flowcode
- PIC mikrokontroler
- LCD displej 16x2

## Autor

Emin Tulumović, ETŠ Tuzla
