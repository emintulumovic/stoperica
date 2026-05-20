# Stop/Start Štoperica

Simulacija rada digitalne štoperice urađena u Flowcode-u. Projekat omogućava precizno mjerenje vremena uz prikaz minuta, sekundi i stotinki na LCD ekranu.

## Opis

Program kontinuirano prati i prikazuje proteklo vrijeme u formatu `MM:SS:ss` (minute:sekunde:stotinke) na LCD displeju. Korisnik može upravljati štopericom putem četiri fizička tastera. Svaki taster čita svoje stanje i na osnovu toga mijenja tok programa.

## Tasteri

| Taster     | Varijabla | Funkcija                                      |
|------------|-----------|-----------------------------------------------|
| SWITCH(0)  | `start`   | Pokretanje štoperice – počinje odbrojavanje   |
| SWITCH(1)  | (loop)    | Međuvrijeme – bilježi trenutno stanje vremena |
| SWITCH(2)  | `stop`    | Zaustavljanje štoperice – pauzira odbrojavanje|
| SWITCH(3)  | `reset`   | Resetovanje – vraća minute, sekunde i stotinke na 0 |

## Tehnologije

- Flowcode
- PIC mikrokontroler
- LCD Display (16x2)

## Autor

Emin Tulumovic
