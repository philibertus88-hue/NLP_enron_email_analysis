# NLP Enron email analysis
This project demonstrates how we can use NLP to extract information from the public enron email dataset to uncover topics and interactions between people.

## 🔍 Ziele des Projekts

- Extraktion relevanter Entitäten wie **Personen**, **Organisationen** und **Orte** mittels spaCy-NER  
- Analyse von Kommunikationsmustern (Wer schreibt wem?)  
- Aufbau eines **Beziehungsnetzwerks** zwischen Personen  
- Identifikation thematischer Schwerpunkte und potenziell verdächtiger Inhalte  
- Vorbereitung einer Pipeline, die in realen Ermittlungen eingesetzt werden könnte

---

## 🧠 Methoden & Technologien

- **Python 3.10+**
- **spaCy** (`en_core_web_lg`) für Named Entity Recognition  
- **pandas** für Datenverarbeitung  
- **networkx** für Graphanalyse  
- **matplotlib / seaborn** für Visualisierungen  
- **regex** für Textbereinigung  
- **Jupyter Notebooks** für explorative Analysen  

---

## 📁 Projektstruktur

NLP_enron_email_analysis/
    data/
        raw/            # Original E-Mails
        out/            # Strukturierte CSV/Parquet-Dateien
    code/
        notebooks/
        functions/
        
    figures/             # Visualisierungen (Netzwerke, Plots)
    README.md
    requirements.txt


---

## 🧩 Pipeline im Überblick

### 1. **Datenextraktion**
Alle .txt-Dateien werden eingelesen, Header und Body getrennt und in ein DataFrame überführt:

- `sender`
- `receiver`
- `timestamp`
- `subject`
- `body`

### 2. **Textbereinigung**
- Entfernen von Signaturen  
- Entfernen von Zitatblöcken (`>`)  
- Normalisierung von Leerzeichen  

### 3. **Named Entity Recognition (NER)**
Mit spaCy werden folgende Entitäten extrahiert:

- `PERSON` – Personen  
- `ORG` – Firmen/Organisationen  
- `GPE` – Orte/Länder/Städte  

### 4. **Kommunikationsanalyse**
- Häufigste Sender/Empfänger  
- Kommunikationsintensität über die Zeit  
- Keyword-Analysen  

### 5. **Netzwerkgraphen**
Aus gemeinsamen Entitäten oder Sender/Empfänger-Beziehungen wird ein Graph aufgebaut:

- zentrale Akteure  
- Cluster  
- potenzielle Schlüsselpersonen  

---

## 📊 Beispielergebnisse

*(Hier kannst du später 1–2 PNGs aus `reports/figures/` einfügen.)*

- Netzwerkgraph der wichtigsten Personen  
- Häufigste Organisationen  
- Timeline der Kommunikation  
- Keyword-Häufigkeiten  

---


