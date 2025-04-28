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
 
## 📁 Modelle
- **Beschreibung:**  
  Enthält die trainierten Modelle basierend auf den annotierten Korpora.

- **Inhalt:**  
  - `hagedorn-gesamt-mit-zeilen.mlmodel`  
    → Modell, trainiert mit Zeilenannotation.
  - `hagedorn-gesamt-ohne-zeilen-ubma.mlmodel`  
    → Modell, trainiert ohne Zeilenannotation (mit UBMA-Optimierung).
  - `hagedorn-gesamt-ohne-zeilen.mlmodel`  
    → Modell, trainiert ohne Zeilenannotation (Standard).
  - `mehrspaltig_ubma.mlmodel`  
    → Modell für mehrspaltige Layouts, UBMA-optimiert.

- **Verwendung:**  
  Modelle können direkt für Vorhersagen oder Feinevaluationen genutzt werden.

## 📁 Testkorpus
- **Beschreibung:**  
  Enthält Testdatensätze sowie die automatisch erzeugten Annotationen durch die trainierten Modelle.

- **Struktur:**
  - **Bilder (unannotierter Testkorpus):**
    - `Testkorpus 43`
    - `Testkorpus 92_1`
    - `Testkorpus 92_2`
    - → Enthalten jeweils Bilddateien ohne Annotationen.
  
  - **Modelle (automatische Annotationen):**
    - `hagedorn-gesamt-mit-zeilen`
    - `hagedorn-gesamt-ohne-zeilen-ubma`
    - `hagedorn-gesamt-ohne-zeilen`
    - `mehrspaltig_ubma`
    - → In jedem Modell-Ordner befinden sich `.zip`-Dateien mit automatisch erzeugten Annotationsdaten.

- **Verwendung:**  
  Die unannotierten Testkorpora dienen der Evaluierung der Modellleistung.  
  Die automatisch erstellten Annotationen ermöglichen eine einfache Weiterverarbeitung und Analyse der Modellergebnisse.


