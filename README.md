# 🏛️ Sistema di Raccomandazione dei Luoghi Culturali Italiani

Sistema di raccomandazione personalizzata dei luoghi culturali in Italia, sviluppato in Python con interfaccia interattiva Streamlit. Suggerisce le strutture più pertinenti in base alle preferenze tematiche dell'utente, alla prossimità geografica e all'accessibilità.

## 🚀 Demo interattiva

👉 [Apri il sistema di raccomandazione](https://sistema-di-raccomandazione-luoghi-culturali-fuungvqmmvp9tshto3.streamlit.app/)

---

## 📌 Descrizione

Il progetto sviluppa un sistema di raccomandazione content-based per i luoghi culturali italiani (musei, gallerie, biblioteche, teatri, monumenti e siti archeologici), con l'obiettivo di valorizzare anche i poli culturali minori o meno conosciuti, spesso trascurati a favore delle destinazioni più frequentate.

Il sistema costruisce un profilo utente personalizzato attraverso preferenze tematiche e tipologiche esplicite, combinandole con un fattore di prossimità geografica per restituire raccomandazioni pertinenti e spazialmente accessibili. Per ciascun risultato vengono esplicitati i criteri della raccomandazione, garantendo trasparenza algoritmica e favorendo la fiducia dell'utente nello strumento.

---

## 🎯 Obiettivi

- Sviluppare un sistema di raccomandazione personalizzata dei luoghi culturali italiani basato su approccio content-based
- Integrare la dimensione geografica nel meccanismo di raccomandazione attraverso matrici di distanza e filtri per area di ricerca
- Costruire profili utente tramite matrici di caratteristiche (Feature Matrices) e calcolo della similarità (Cosine Similarity)
- Valorizzare i luoghi culturali minori o periferici, offrendo alternative alle destinazioni più frequentate
- Realizzare un'interfaccia interattiva trasparente che espliciti i criteri alla base di ogni suggerimento

---

## 🔬 Metodologia

**Profilo utente e preferenze**
Il profilo utente viene definito tramite la selezione di un profilo culturale predefinito (tipologie di visitatore), personalizzabile attraverso una scala Likert a cinque livelli per temi di interesse e selezione delle tipologie di luoghi preferite. I pesi vengono normalizzati tra 0 e 1 e combinati con la definizione dell'area geografica di interesse (regione, comune o indirizzo puntuale geocodificato) e un raggio di ricerca in km.

**Calcolo delle raccomandazioni**
A ciascun luogo culturale del dataset, filtrato per area geografica e raggio di ricerca, viene assegnato uno score sintetico che integra la corrispondenza tra il profilo utente e gli attributi descrittivi del luogo, ponderata da un fattore di prossimità geografica calcolato sulla distanza dal centro di ricerca. I risultati vengono ordinati per score decrescente e presentati come graduatoria configurabile.

**Presentazione dei risultati**
I risultati sono visualizzati tramite mappa interattiva (luoghi geolocalizzati e colorati per tipologia) e schede descrittive con punteggio, distanza, tipologia, tema principale, motivazione testuale e indicazione dell'accessibilità per disabili.

---

## 📊 Risultati principali

- Realizzato un geodatabase multidimensionale dei beni culturali italiani con attributi tassonomici, metriche di accessibilità e dati geografici
- Sviluppato il motore di raccomandazione content-based in Python, con calcolo dinamico dei vettori di preferenza e vincoli di geolocalizzazione
- Implementata l'applicazione web interattiva in Streamlit con moduli per posizione, filtri tematici e raggio di ricerca
- Generato un sistema di ranking reattivo con output descrittivi e trasparenti, predisposto per futura integrazione di algoritmi avanzati (filtraggio collaborativo, implicit/explicit feedback)

---

## 🛠️ Tecnologie utilizzate

- **Python** — sviluppo del motore di raccomandazione e pipeline dati
- **Streamlit** — interfaccia web interattiva
- **Pandas / NumPy** — gestione e modellazione dei dati
- **Folium** — visualizzazione geografica interattiva
- **OpenCage** — geocodifica degli indirizzi
- **OpenStreetMap / Overpass API** — dataset dei luoghi culturali
- **ISTAT** — dati territoriali e demografici di supporto

---

## 📁 Struttura del progetto

```
Raccomandazione_Luoghi_Culturali_Italia/
├── README.md
├── app_raccomandazione.py
├── recommender.py
├── user_profile.py
└── requirements.txt
```

> ⚠️ I dataset di input (GeoJSON dei luoghi culturali, dati ISTAT) non sono inclusi nel repository per ragioni di dimensione. Le fonti sono indicate nella sezione Dati.

---

## 📂 Dati

| Fonte | Descrizione |
|-------|-------------|
| [OpenStreetMap / Overpass API](https://overpass-api.de) | Database dei luoghi culturali italiani (musei, gallerie, biblioteche, teatri, monumenti, siti archeologici) |
| [ISTAT](https://www.istat.it) | Dati territoriali e demografici comunali e regionali |
| [OpenCage](https://opencagedata.com) | Geocodifica degli indirizzi per la localizzazione dell'utente |

---

## 🔗 Link utili

- 🚀 [Demo live — Sistema di Raccomandazione](https://sistema-di-raccomandazione-luoghi-culturali-fuungvqmmvp9tshto3.streamlit.app/)
- 🌐 [Sport Business Lab Consultancy](https://www.sblconsultancy.it/)
