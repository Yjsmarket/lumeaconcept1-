# Overdracht

Stand van zaken van de site voor LUMEA Amsterdam, Johan Huizingalaan 192.

## Wat er staat

| Pad | Wat het is |
| --- | --- |
| `/` | Homepage, concept A. Beige en zwart, gecentreerd merkteken. |
| `/concept-b/` | Homepage, concept B. Licht beige en bruin, gedeelde hero, redactioneel. |
| `/concept-c/` | Homepage, concept C. Nacht, crème en goud, volvlak hero met zijrail. |
| `/menu/` | De kaart. Mobiel eerst, foto naast elk gerecht, tikken geeft een grote foto. Gedeeld door alle concepten. |
| `/tafelkaart/` | Printpagina. A4 liggend, twee kaartjes van ongeveer A6 met de QR. |

Er is nog **geen concept gekozen**. Zodra dat gebeurt gaan de andere twee mappen
eruit en verhuist de gekozen homepage naar de hoofdmap.

## Wat nog ontbreekt

Deze staan als zichtbare plaatshouder in de pagina's. Zoek op `[` om ze te vinden.

- `[TIJD]` en `[TIJD INVULLEN]`: openingstijden, op alle drie de homepages
- `[POSTCODE]`: postcode van de zaak
- `[TELEFOON]` en `[TELEFOONNUMMER]`: telefoonnummer
- `[E-MAIL]` en `[E-MAILADRES]`: e-mailadres
- `[INSTAGRAM]`: het Instagram-adres
- `€ --,--`: **alle prijzen op de kaart**. Niet één prijs is echt.

## Foto's

Alle foto's in `assets/fotos/` zijn **stockfotografie van Unsplash**, geen foto's
van de zaak zelf. Ze dienen om het ontwerp te beoordelen. Voordat de site live
gaat moeten er eigen foto's in. De bestandsnamen zeggen welk gerecht erbij
hoort, dus vervangen kan één op één, zelfde naam, zelfde plek. De productfoto's
zijn vierkant, 700 bij 700.

## De QR-code

`assets/qr/qr-menu.svg` verwijst naar:

    https://yjsmarket.github.io/lumeaconcept1-/menu/

Die code is nagelezen met een decoder en komt exact op dat adres uit. Komt er
een eigen domein, of verandert de naam van de repo, **dan moet de QR opnieuw
gemaakt worden**. De oude blijft anders naar een dood adres wijzen, ook op
kaartjes die al gedrukt zijn.

## Techniek

Statische HTML, CSS en JavaScript, geen build-stap. Bedoeld voor GitHub Pages.
Pages staat nog **niet** aan, dat moet nog in de instellingen van de repo.

`assets/js/lumea.js` doet het invloeien bij scrollen en de vergroting op de
kaart. Het onthullen gaat op scrollpositie en niet met een
IntersectionObserver: die geeft bij een sprong naar een anker geen melding voor
de overgeslagen blokken, waardoor die blanco bleven als iemand terugscrolde.
Het verbergen zit achter de klasse `js-aan`, die het script zelf zet. Draait de
JavaScript niet, dan staat de tekst er gewoon.

## Werkafspraken

`CLAUDE.md` in deze map bevat de vaste regels voor schrijfstijl, ontwerp en
techniek. Die wordt automatisch gelezen bij het starten van een sessie.
