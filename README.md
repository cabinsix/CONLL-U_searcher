# CONLL-U_searcher
In this repository I uploaded a code (created through a mostly AI supported generation) for reading and performing some basic research tasks on Conll-U files/corpora. 

English below.


# Python CONLL-U Searcher

## 🇮🇹 Italiano
### Descrizione
Python CONLL-U Searcher è un’applicazione GUI per la ricerca e analisi di corpora annotati in CONLL-U.
Permette di:
* Cercare token per lemma, forma, UPOS, DEPREL, FEATS e MISC
* Filtrare frasi per sent_id
* Analizzare frequenze di token, collocazioni, KWIC (Key Word in Context), dipendenze e feature
* Esportare i risultati in CSV
L’interfaccia grafica è basata su Tkinter, semplice e intuitiva.
Requisiti
* Python 3.8+
* Librerie Python: tkinter (di default), collections, csv, os, re
* File di input in formato CONLL-U
Struttura delle cartelle
project_root/
│
├─ conllu_files/           # Cartella principale con i corpora
│  ├─ corpus1/             # Cartella di un corpus
│  │  ├─ file1.conllu
│  │  └─ file2.conllu
│  └─ corpus2/
│     ├─ file1.conllu
│     └─ file2.conllu
│
├─ main.py                 # Script Python principale
└─ README.md               # Questo file
conllu_files/: contiene le sottocartelle di ciascun corpus

Ogni corpus può avere uno o più file .conllu
Lo script legge automaticamente tutti i file .conllu nelle sottocartelle
Come usare
* Avvia main.py con Python:
* python main.py

* Seleziona uno o più corpora (Ctrl+click per multi-selezione)
* Inserisci i filtri desiderati:
  * Lemma: lemma del token
  * Word: forma del token
  * UPOS: part-of-speech (OR separati da |)
  * FEATS: features grammaticali (k=v separati da |)
  * MISC: campi MISC (k=v o solo k per True)
  * DEPREL: relazione sintattica (OR separati da |)
  * Sent_id: opzionale, per filtrare frasi specifiche
* Scegli le opzioni da calcolare: keyword analysis, KWIC, collocazioni, frequenze DEPREL/FEATS
* Premi Search per visualizzare i risultati in una finestra popup
* Esporta KWIC, keywords, collocazioni, DEPREL e FEATS in CSV tramite i pulsanti presenti nella finestra

#### Note
* I filtri sono case-insensitive e ignorano spazi extra
* KWIC e collocazioni possono essere filtrate per POS
* La frequenza dei token può escludere la punteggiatura (PUNCT) se selezionata


## 🇬🇧 English
### Description
Python CONLL-U Searcher is a GUI application to search and analyze corpora annotated in CONLL-U format.
It allows you to:
* Search tokens by lemma, form, UPOS, DEPREL, FEATS, and MISC
* Filter sentences by sent_id
* Analyze token frequencies, collocations, KWIC (Key Word in Context), dependencies, and features
* Export results in CSV format

The GUI is built with Tkinter, simple and intuitive.

Requirements
* Python 3.8+
* Python libraries: tkinter (default), collections, csv, os, re
* Input files must be in CONLL-U format
* Folder structure
project_root/
│
├─ conllu_files/           # Main folder containing corpora
│  ├─ corpus1/             # Folder for a single corpus
│  │  ├─ file1.conllu
│  │  └─ file2.conllu
│  └─ corpus2/
│     ├─ file1.conllu
│     └─ file2.conllu
│
├─ main.py                 # Main Python script
└─ README.md               # This file

* conllu_files/: contains a subfolder for each corpus
* Each corpus can contain one or more .conllu files
The script automatically reads all .conllu files in subfolders

How to use
* Run main.py with Python:
* python main.py
* Select one or more corpora (Ctrl+click for multi-selection)
* Enter the desired filters:
  * Lemma: token lemma
  * Word: token form
  * UPOS: part-of-speech (OR separated by |)
  * FEATS: grammatical features (k=v separated by |)
  * MISC: MISC fields (k=v or just k for True)
  * DEPREL: syntactic relation (OR separated by |)
  * Sent_id: optional, to search specific sentences
* Choose options to calculate: keyword analysis, KWIC, collocations, DEPREL/FEATS frequencies
* Press Search to view results in a popup window
* Export KWIC, keywords, collocations, DEPREL, and FEATS to CSV using buttons in the window

#### Notes
Filters are case-insensitive and ignore extra spaces
KWIC and collocations can be POS-filtered
Token frequencies can optionally exclude punctuation (PUNCT)



CONLL-U searcher. 2026. https://github.com/cabinsix/CONLL-U_searcher. 
