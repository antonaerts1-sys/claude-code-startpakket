# Hoe dit werkt (voor wie het wil weten)

Claude Code onthoudt niets tussen twee gesprekken. Alles wat je uitlegt (wie de klant is,
wat al beslist is, waarom die ene aanpak is afgeschoten) is bij het volgende gesprek weg,
en dus leg je het opnieuw uit, elke keer net iets anders, met elke keer net iets andere
antwoorden als gevolg.

De oplossing is één zin: wat op schijf staat blijft, wat in de chat staat verdwijnt.
Claude leest bij elke start automatisch het bestand `CLAUDE.md` in je projectmap. Dit
pakket is niets meer dan georganiseerd gebruik van dat mechanisme, en Claude zet het op
en onderhoudt het zelf. Jouw enige taken: materiaal aanleveren en vragen beantwoorden.

## Twee lagen

Alles in een projectmap valt in twee soorten, en het hele systeem is dat onderscheid:

**Bevroren** (schrijf je één keer, herschrijf je nooit):
- `docs/bronnen/`: mails, transcripten, verslagen, exports, ongewijzigd, met datum in
  de naam. Dit is het bewijsmateriaal.
- `docs/log.md`: één regel per werksessie. Fouten worden niet gewist; de correctie is
  de volgende regel. Hieruit reconstrueer je later de volgorde van het denken.

**Levend** (houdt Claude actueel, oude stand mag weg):
- `CLAUDE.md`: wat het project is, de actuele status, de beslissingen, de valkuilen.
- `docs/open-vragen.md`: wat nog niet beslist is, met vaste nummers.
- Takeaways naast lange bronnen: de korte werklaag, zodat niet elke sessie het hele
  transcript hoeft te herlezen.

De levende laag mag gerust herschreven worden, juist ómdat de bevroren laag bewijst waar
elke conclusie vandaan kwam. Als iemand vraagt "waar staat dat precies", kan je het
aanwijzen.

## De gewoontes in het kort

1. Bronnen filen vóór je ermee werkt, nooit achteraf bewerken.
2. Takeaways naast lange bronnen, gemarkeerd als interpretatie.
3. Log bijhouden, append-only.
4. Vaste nummers in registers, nooit hernummeren (anders is "punt 4" uit een mail van
   vorige maand ineens een ander punt).
5. Observatie gescheiden van interpretatie, met bron; gaten expliciet benoemen.
6. Afsluitritueel: aan het eind van elke sessie actualiseert Claude status, beslissingen,
   open vragen en log in één beweging.

## Wanneer je dit niet gebruikt

Voor eenmalige klussen: een tekstje, een snelle vraag, iets dat vandaag af is. Structuur
opzetten voor iets dat morgen klaar is, is overhead zonder opbrengst, en Claude hoort dat
zelf ook te zeggen als je het vraagt.

Vuistregel: zodra je jezelf iets een tweede keer hoort uitleggen aan Claude, verdient het
project een CLAUDE.md.
