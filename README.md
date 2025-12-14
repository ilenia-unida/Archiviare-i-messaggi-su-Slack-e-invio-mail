# 📢 Flusso Automatico: Archiviazione Messaggi Slack

Un workflow di automazione robusto, costruito con **n8n**, progettato per catturare in tempo reale i messaggi da un canale Slack designato, trasformarli immediatamente in file di testo (TXT) e archiviarli su Google Drive, inviando contemporaneamente una notifica via email.

## ✨ Caratteristiche & Funzionalità

* **Trigger Slack:** Si attiva ogni volta che viene inviato un messaggio nel canale Slack configurato.
* **Archiviazione Duplice:** Il messaggio viene archiviato in due modi:
    * **Cloud Storage:** Viene creato un file TXT su Google Drive.
    * **Notifica Email:** Viene inviato via Gmail come allegato a un destinatario predefinito.
* **Conversione Automatica:** Il nodo "Centro di commando" (Code) legge il testo del messaggio e lo incapsula in un file TXT con un nome univoco basato sulla data e ora.

## 🚀 Struttura del Flusso

Il flusso è composto dai seguenti nodi:

1.  **Slack Trigger:** 💬 Attivato alla ricezione di un messaggio.
2.  **Centro di commando (Code):** 🧩 Prepara il testo del messaggio per l'archiviazione, creando i dati binari di un file TXT.
3.  **Google Drive - Crea File:** 💾 Carica il file TXT creato nella cartella specificata su Drive.
4.  **Gmail - Invia Email:** 📧 Invia il file TXT come allegato via email al destinatario configurato.

## 📺 Video di Spiegazione

Per una spiegazione dettagliata del funzionamento, della logica e della configurazione dei nodi, guarda il video qui sotto:

[Spiegazione dettagliata del flusso su YouTube](https://youtu.be/Z2BvPtWAgmE)

## 🛠️ Requisiti

Per poter utilizzare questo flusso, dovrai configurare le seguenti credenziali nel tuo ambiente n8n:

* **Slack Account** (per il `Slack Trigger`)
* **Google Drive Account**
* **Gmail Account**
