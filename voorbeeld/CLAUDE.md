# Aanmeldformulier vzw Kompas

<!-- Fictief voorbeeld: zo ziet een opgezet project er in de praktijk uit. -->

Vzw Kompas (jeugdwerking, 4 locaties) meldt vrijwilligers nu aan met een papieren
formulier dat per post of ingescand binnenkomt. Coördinator Lieve typt alles over in een
Excel. We bouwen een webformulier dat rechtstreeks in hun bestaande ledenlijst schrijft.
Oplevering afgesproken voor half oktober 2026.

## Lees eerst, in deze volgorde

1. `docs/log.md` (laatste regels): waar we stonden bij de vorige sessie
2. `docs/bronnen/2026-08-14-gesprek-lieve-takeaways.md`: de kern van het enige gesprek
   met de opdrachtgever; het volledige transcript staat ernaast voor als het erop aankomt
3. `docs/bronnen/2026-08-14-huidig-formulier.pdf`: het papieren formulier dat we
   vervangen, alle velden staan erin
4. `docs/open-vragen.md`: wat nog niet beslist is, met vaste nummers

## Status

Velden in kaart gebracht en teruggekoppeld aan Lieve. Het formulier staat als klikbaar
prototype in `prototype/`. Wacht op antwoord van hun IT over schrijfrechten op de
ledenlijst (V3); zolang dat er niet is, schrijven we naar CSV.

## Beslissingen die vastliggen

- B1. Geen account of login voor de vrijwilliger: Lieve was hier stellig over, de drempel
  moet zo laag mogelijk. Een link volstaat.
- B2. Geen rijksregisternummer opvragen, ook al staat het op het papieren formulier:
  wordt nergens gebruikt en maakt het een AVG-dossier.
- B3. Per locatie een eigen formulierlink, niet één formulier met keuzelijst: de vier
  locaties werken los van elkaar en willen elk hun eigen instroom zien.

## Belangrijk om niet te vergeten

- Ongeveer een derde van de vrijwilligers is ouder dan 65 en vult dit op een tablet in:
  grote knoppen, niets dat je niet kan overslaan.
- "Lid" en "vrijwilliger" is bij Kompas niet hetzelfde: een lid betaalt lidgeld, een
  vrijwilliger niet. In hun Excel staan ze door elkaar. Nooit stilzwijgend samenvoegen.
- De ledenlijst is van een externe partij die traag antwoordt: plan daar niets
  kritisch omheen.

## Werkafspraken

- Alles in het Nederlands, ook code-commentaar.
- Bronmateriaal eerst ongewijzigd in `docs/bronnen/` met datum in de naam, dan pas
  ermee werken. Bronbestanden nooit achteraf bewerken.
- Bij lange bronnen een takeaways-bestand ernaast, gemarkeerd als interpretatie.
- Aan het eind van elke sessie: status en beslissingen hierboven actualiseren, open
  vragen bijwerken, één regel onderaan `docs/log.md`. Log is append-only.
- Open vragen (V#) en beslissingen (B#) houden hun nummer voor altijd.
- Verzin geen veldnamen of regels die niet uit het gesprek of het formulier komen;
  wat ontbreekt wordt een open vraag.
- Denk eerst mee. Bouw pas als het gevraagd wordt.

## Technisch

- Los HTML-bestand met een klein stukje JavaScript, geen framework: moet op hun
  bestaande hosting kunnen staan.
- Openen: `prototype/index.html` in de browser.
- Niet aanraken: `docs/bronnen/` (bevroren).
