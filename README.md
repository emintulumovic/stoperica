# Štoperica — Flowcode & PIC mikrokontroler

Projekat urađen u Flowcode-u kao simulacija digitalne štoperice na PIC16F88 mikrokontroleru. Rađeno u sklopu laboratorijske vježbe iz Praktične nastave.

## Šta radi

Štoperica mjeri proteklo vrijeme i prikazuje ga na LCD ekranu u formatu minute:sekunde:stotinke. Upravljanje je putem četiri tastera:

| Taster | Funkcija |
|--------|----------|
| Start | Počinje mjerenje |
| Stop | Pauzira mjerenje na trenutnoj vrijednosti |
| Lap | Sprema međuvrijeme, tajmer nastavlja u pozadini |
| Reset | Resetuje sve na nulu |

## Kako je implementovano

U glavnoj petlji program čita stanje svakog tastera i na osnovu toga mijenja tok izvršavanja. Brojanje radi tako što se stotinke povećavaju korak po korak — kad dođu do 100, sekunde se povećaju i stotinke se vrate na nulu. Isti princip vrijedi za sekunde i minute. Lap funkcija kopira trenutne vrijednosti u poseban set varijabli i prikazuje ih na ekranu dok mjerenje teče normalno.

## Hardverske komponente

- Mikrokontroler: PIC16F88
- LCD ekran: 16x2, port B, 4-bitna komunikacija
- Tasteri: digitalni tasteri na portu A

## Screenshotovi

### Globalne varijable u projektu

![Globalne varijable](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/preview.webp)

Varijable korištene u projektu: stanja štoperice (start, stop, reset, loop) i mjerenje (minute, sekunde, stotinke). Svaka mjerna varijabla ima i duplikat (npr. minute1) za potrebe Lap funkcije.

### Flowcode dijagram toka

![Dijagram toka](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/prva.webp)

Grafički prikaz cijelog programa — od inicijalizacije do glavne petlje sa svim grananjima i ispisom na LCD.

### Štoperica u toku mjerenja

![Mjerenje u toku](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/druga.webp)

Screenshot simulacije dok štoperica radi. Na LCD-u se vidi izmjereno vrijeme, što potvrđuje da tajmer i ispis rade ispravno.

### Početno stanje nakon reseta

![Reset stanje](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/treca.webp)

Ekran prikazuje 00:00:00 — sve varijable su na nuli i sistem čeka na Start.

### Lap funkcija — međuvremena

![Lap vremena](https://raw.githubusercontent.com/redzictarik/FlowCode--STOPERICA/main/cetvrta.webp)

Prikaz više uzastopnih međuvremena. Svako je zabilježeno dok je tajmer nastavio normalno raditi u pozadini.

## Tehnologije

- Flowcode
- PIC16F88

## Autor

Emin Tunguzović, ETŠ Tuzla
