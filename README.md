# ZIPP — Samen studeren

Een eenvoudige, mobielvriendelijke studiepagina in de zwart-witte huisstijl van ZIPP.

## Toetsen en studeermethodes aanpassen

Open `toetsen.json` in de hoofdmap van het project. Elke toets kan een of meer studeermethodes bevatten:

```json
[
  {
    "vak": "Wiskunde",
    "datum": "2026-11-25",
    "leerstof": "Hoofdstuk 3, oefeningen 1–8",
    "methodes": [
      {
        "type": "flashcards",
        "titel": "Formules oefenen",
        "kaarten": [
          {
            "vraag": "Wat is de formule voor de oppervlakte van een cirkel?",
            "antwoord": "Oppervlakte = π × straal²"
          }
        ]
      },
      {
        "type": "quiz",
        "titel": "Oefentest",
        "vragen": [
          {
            "vraag": "Hoeveel is 7 × 8?",
            "opties": ["54", "56", "64"],
            "juist": 1,
            "uitleg": "7 × 8 = 56."
          }
        ]
      }
    ]
  }
]
```

Ondersteunde methodes:

- **Flashcards** (`"type": "flashcards"`): geef `kaarten` op met per kaart een `vraag` en `antwoord`. In ZIPP kun je het antwoord tonen en door de kaarten bladeren.
- **Oefentest** (`"type": "quiz"`): geef `vragen` op met per vraag tekst, een lijst `opties` en `juist`. `juist` is het nummer van de goede optie, beginnend bij `0` (dus `1` betekent de tweede optie). `uitleg` is optioneel. ZIPP geeft feedback en toont je score.

De datum gebruikt het formaat `JJJJ-MM-DD`. `leerstof` en `methodes` zijn optioneel. Je kunt meerdere toetsen in de lijst zetten; zet een komma tussen de toets-objecten. Sla het JSON-bestand op en publiceer de wijzigingen naar GitHub om ze op de website te zien. Let op: JSON vereist dubbele aanhalingstekens en geen komma na het laatste item.

## Logo vervangen

Plaats het logo in de map `assets` in dit project, naast `assets/README.md`, en noem het bestand **`logo.png`**. De website gebruikt die afbeelding automatisch in de kop, op het toegangsscherm en in de banner.

Bijvoorbeeld op GitHub: open de map `assets`, kies **Add file → Upload files**, upload je afbeelding en zorg dat de bestandsnaam `logo.png` is. Commit de wijziging daarna. Een vierkante PNG werkt meestal het best. Gebruik je JPG of WebP, pas dan in `index.html` de regel `const LOGO_PATH = "assets/logo.png";` aan naar het pad en de bestandsnaam van jouw afbeelding.

Als er nog geen logo op die plek staat, toont de website tijdelijk een Z als markering.

## Online zetten met GitHub Pages

1. Push de repository naar GitHub.
2. Open **Settings → Pages** in de repository.
3. Kies bij **Build and deployment** voor **Deploy from a branch**.
4. Kies de branch `main` en de map `/ (root)`, en klik op **Save**.
5. Na het publiceren verschijnt de website-link op diezelfde Pages-pagina.

## Over de toegangscode

De code `3NWA` is alleen een eenvoudige drempel voor klasgenoten. Omdat GitHub Pages statische bestanden publiceert, is deze code zichtbaar in de broncode en beschermt ze de inhoud niet echt. Zet hier dus geen privégegevens op. Voor echte afgeschermde toegang is een host met authenticatie nodig.