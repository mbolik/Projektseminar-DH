## 📁 Ground Truth
- **Beschreibung:**  
  Enthält die Gesamtheit aller annotierten Daten des Projekts.

- **Struktur:**
  - **Bilder/**
    - Enthält unannotierte Bilddateien, unterteilt in fünf Verlegerkategorien:
      - Bohn
      - Jr. Bohn
      - Schmieder
      - Fleischhauer
      - Schrämbl
  - **PAGE/**
    - Enthält Annotationen im PAGE-Format (.zip-Dateien), ebenfalls nach den fünf Verlegern sortiert:
      - Bohn
      - Jr. Bohn
      - Schmieder
      - Fleischhauer
      - Schrämbl

- **Verwendung:**  
  - "Bilder" dient als Grundlage für das Training und Testing der Modelle.
  - "PAGE" stellt die dazugehörigen strukturierten Annotationsdaten bereit, die für die Auswertung und das Training benötigt werden, sowohl Zeilen- als auch Flächeannotationen.
  - 
## 📁 Korpus (balanciert)
- **Beschreibung:**  
  Enthält die ausbalancierten Annotationsdaten und Transkriptionen des Projekts.

- **Struktur:**
  - Enthält ZIP-Dateien:
    - Mit Zeilenannotation
    - Ohne Zeilenannotation
  - Die Dateien sind nach Verlegern sortiert:
    - Bohn Jr.
    - Bohn
    - Schmieder
    - Fleischhauer
    - Walthard
    - Schrämpl
    - Trattner
    - Baumeister

- **Verwendung:**  
  - Dient als Grundlage für Experimente, bei denen ein ausgeglichenes Verhältnis zwischen den Verlegern gewährleistet sein soll.
  - Ermöglicht Training sowohl auf Zeilen- als auch auf Flächenebene.
