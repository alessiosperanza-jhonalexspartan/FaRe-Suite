<div align="center">

# Fa.Re. Suite

**Strumenti forensi e investigativi per le Forze dell'Ordine**

[![Sito](https://img.shields.io/badge/Sito-alessiosperanza.it-blue)](https://alessiosperanza.it)
[![Piattaforma](https://img.shields.io/badge/Piattaforma-Windows%2010%2F11-lightgrey)](#requisiti)
[![Licenza](https://img.shields.io/badge/Licenza-Proprietaria-red)](#licenza)
[![Privacy](https://img.shields.io/badge/Elaborazione-100%25%20locale-green)](#filosofia)

</div>

---

**Fa.Re.** è una suite di software professionali sviluppata in Italia e pensata per l'attività operativa e investigativa di **Polizia Locale** e **Polizia Giudiziaria**.

---

## I software

### 🔍 Fa.Re. Vision
Analisi biometrica e riconoscimento facciale forense.

- **Ricerca facciale** su archivi fotografici e video, con filtri per fascia d'età e sistema di guardie anti falsi positivi (qualità immagine, posa, punteggio di rilevamento)
- **Riconoscimento live** multi-camera con tracciamento dei soggetti, ricerca vettoriale FAISS e profili operativi preconfigurati (Ingresso controllato, Ambiente aperto GPU/CPU)
- **Video Clustering**: raggruppamento automatico dei volti presenti in filmati lunghi
- **Antropometria forense**: stima dell'altezza da singola immagine (metrologia single-view) con intervalli di confidenza Monte Carlo, in linea con le raccomandazioni ENFSI
- Interfaccia completamente bilingue **IT/EN**

### 💾 Fa.Re. ForensKit
Suite di digital forensics per acquisizione, analisi e trascrizione.

- **Artefatti Windows**: analisi delle tracce di sistema e di utilizzo
- **Browser & OSINT**: estrazione e analisi di cronologia e artefatti di navigazione
- **Imaging logico** e analisi di file sospetti
- **Audio Forensics 2.0**: trascrizione automatica locale con Whisper e faster-whisper, gestione automatica di file lunghi (auto-chunking oltre i 30 minuti), coda batch multi-file, conversione dei vocali WhatsApp (opus → WAV), player integrato con controllo velocità
- **Video Downloader forense**: acquisizione di video e commenti da piattaforme online (yt-dlp) con esportazione in txt/csv/html/json e **manifest di catena di custodia**

### 📡 Fa.Re. NEXUS
Analisi di tabulati telefonici (CDR) e mobile forensics.

- **Parser CDR** per TIM, Vodafone, WindTre, Iliad e Fastweb, resiliente alle variazioni di formato degli operatori
- **Ricerche avanzate** su numeri, IMEI, IMSI, celle e sessioni dati (9 schede dedicate)
- **Co-presenze su traffico di cella**: individuazione di utenze compresenti sotto la stessa BTS, con parser universale per i formati di traffico cella dei diversi operatori
- **Assistente in linguaggio naturale** (opzionale): interrogazione dei dati in italiano tramite LLM **eseguito in locale** (Ollama), con protezioni SQL multilivello e audit trail completo delle interrogazioni
- **Modulo Mobile Forensics**: importazione di estrazioni Cellebrite, dashboard, timeline, grafo relazionale, analisi chat e messaggi cancellati, mappa, e **Bridge CDR** per incrociare tabulato e contenuto del dispositivo
- **Android ADB Forensics** con Forensic Write Guard, audit log firmato SHA-256 e manifest di catena di custodia
- **Sessioni di lavoro cifrate** (AES) vincolate alla macchina e **report DOCX** conformi alla prassi forense italiana

> ⚠️ **NEXUS è in fase di beta testing**: tutti i risultati delle analisi devono sempre essere verificati incrociandoli con il tabulato originale fornito dall'operatore telefonico.

### 🗺️ Fa.Re. AREA
Analisi spaziale della criminalità per uso operativo e di intelligence.

- **Hotspot analysis**: Kernel Density Estimation (KDE), Getis-Ord Gi*, Emerging Hot Spot Analysis (EHSA) con correzione per autocorrelazione temporale, STKDE spazio-temporale
- **Clustering DBSCAN** con calibrazione automatica dei parametri e analisi bivariata
- **Forecast** a supporto della pianificazione dei pattugliamenti e dell'allocazione delle risorse
- **Normalizzazione demografica**: importazione delle griglie di popolazione ISTAT (shapefile) e calcolo dei tassi per 1.000 abitanti in tutti gli analizzatori
- **Domini tematici**: sicurezza urbana ed **Emergenze e Soccorso** (Vigili del Fuoco, Protezione Civile)
- **Report automatici** in formato DOCX/PDF pronti per il briefing operativo

### 🐧 Fa.Re. OS — Argus
Distribuzione Linux live dedicata alla digital forensics (basata su Debian 13).

- **Ambiente live avviabile da USB**: nessuna installazione, nessuna alterazione della macchina analizzata
- **Launcher CLI dedicato** per l'avvio rapido di tutti gli strumenti, organizzati per categoria

**Strumenti integrati:**

| Categoria | Tool |
|---|---|
| **Mobile Forensics** | UFADE (GUI) · ALEAPP (GUI) · iLEAPP (GUI) · Andriller · Android Triage · Androwarn · apkleaks · kobackupdec · adb · libimobiledevice · ifuse |
| **WhatsApp** | whapa-gui (GUI) · whapa CLI · whacipher |
| **Telegram** | telegram-export |
| **OSINT** | Sherlock · Maigret · holehe · theHarvester · SpiderFoot · recon-ng · Photon · metagoofil · PhoneInfoga · h8mail · waybackpy · Instaloader · WhatWeb · dnsrecon · dnstwist · Sublist3r |
| **Memory Forensics** | Volatility3 · volshell · pypykatz · evtxtract · avml · aeskeyfind · rsakeyfind |
| **Rete** | nmap · tcpdump · tcpflow |
| **Preparazione supporti** | GParted (GUI) · nwipe · secure-delete |
| **Varie** | yt-dlp · bruteforce-wallet |

---

## Come richiedere i software

1. **Registrati** sul portale ufficiale: [alessiosperanza.it](https://alessiosperanza.it)
2. **Compila la richiesta** indicando ente/qualifica professionale e finalità d'uso
3. **Attendi l'approvazione**: ogni account viene verificato manualmente prima dell'attivazione
4. **Scarica i software** per cui hai ottenuto l'autorizzazione dall'area riservata
5. **Attiva la licenza**: le licenze sono nominali e vincolate alla macchina (HWID)

Per informazioni, demo o richieste istituzionali è possibile utilizzare il modulo di contatto sul sito.

---

## Requisiti

- **Sistema operativo:** Windows 10/11 (64 bit) per Vision, ForensKit, NEXUS e AREA
- **Fa.Re. OS — Argus:** distribuzione live avviabile da USB (nessun sistema operativo richiesto sulla macchina di analisi)
- **Distribuzione:** eseguibili standalone (nessuna installazione di Python richiesta)
- **Connessione internet:** necessaria solo per l'attivazione della licenza; tutta l'elaborazione dei dati avviene **offline, in locale**

I requisiti hardware specifici (RAM, GPU) variano in base al modulo utilizzato e sono indicati nella documentazione di ciascun prodotto.

---

## Filosofia

- 🔒 **Privacy by design** — nessun dato investigativo lascia mai la macchina dell'operatore
- ⚖️ **Conformità GDPR** — pensato per il trattamento di dati in ambito giudiziario e di polizia
- 🧠 **AI come ausilio, non come sostituto** — ogni risultato è verificabile e documentato
- 📋 **Catena di custodia** — log, hash e manifest per la ripetibilità delle operazioni

---

## Licenza

I software della suite Fa.Re. sono **proprietari** e distribuiti su licenza. Questo repository non contiene codice sorgente: ha esclusivamente finalità informative e di presentazione.

È vietata la ridistribuzione, la decompilazione e la cessione a terzi delle licenze.

---

## Contatti

- 🌐 Sito ufficiale: [alessiosperanza.it](https://alessiosperanza.it)
- 💬 Community Telegram: riservata agli utenti autorizzati (link fornito dopo l'approvazione)

---

<div align="center">
<sub>© Alessio Speranza — Fa.Re. Suite. Tutti i diritti riservati.</sub>
</div>
