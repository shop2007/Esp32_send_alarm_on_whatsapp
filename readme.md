# Camper Alarm ESP32-C3
## La sicurezza intelligente per camper, van e veicoli ricreazionali

Proteggere il proprio camper significa poter contare su un sistema affidabile, configurabile e sempre pronto a segnalare situazioni anomale. **Camper Alarm ESP32-C3** nasce per offrire una soluzione compatta e versatile per il controllo dell’allarme, con gestione locale, Bluetooth, Wi-Fi e notifiche WhatsApp.

---

### Protezione contro le intrusioni
Il sistema controlla un ingresso PIR o un contatto di allarme e rileva automaticamente l’apertura o l’attivazione del sensore.

È possibile configurare:
- Il livello di allarme attivo:
  - Allarme attivo con ingresso a `0` (0 volt)
  - Allarme attivo con ingresso a `1` (+12volt)
- Ritardo di uscita prima dell’inserimento effettivo
- Ritardo di ingresso prima dell’attivazione della sirena
- Durata dell’attivazione del relè sirena

Questa flessibilità permette di adattare il dispositivo a sensori normalmente aperti, normalmente chiusi e a diverse configurazioni elettriche dell’impianto.

---

### Relè configurabile
L’uscita relè può essere adattata al tipo di dispositivo collegato:
- Sirena
- Lampeggiante
- Blocco motore
- Segnalatore luminoso
- Dispositivo ausiliario
- Ingresso di un sistema di allarme esistente

Con il comando dedicato è possibile invertire il funzionamento dell’uscita:
- Relè attivo durante l’allarme
- Relè attivo quando l’allarme è a riposo

La configurazione viene salvata in EEPROM e rimane memorizzata anche dopo lo spegnimento.

---

### Diagnostica durante l’installazione
La modalità diagnostica consente di verificare rapidamente il corretto collegamento tra sensore e relè.

Il comando `18` del menù fa seguire al relè lo stato dell’ingresso PIR. In questo modo l’installatore può controllare:
- Se il sensore cambia realmente stato
- Se il livello attivo è impostato correttamente
- Se il relè è normalmente aperto o normalmente chiuso
- Se l’eventuale inversione dell’uscita è configurata correttamente

La modalità diagnostica si interrompe semplicemente digitando `Q`.

---

### Notifiche WhatsApp
In caso di intrusione, il sistema può inviare automaticamente un messaggio WhatsApp.

Sono supportate:
- Notifica dell’allarme 
- Invio su comando di un messaggio di prova
- Promemoria periodici durante un allarme prolungato
- Gestione di un secondo destinatario
- Abilitazione o disabilitazione dei messaggi whatsapp (durante la messa a punto può essere utile)
- Configurazione separata del numero e delle API key per i due utenti whatsapp

Questa funzione consente di ricevere una segnalazione anche quando ci si trova lontani dal camper.

---

### Controllo Bluetooth
Il dispositivo integra una connessione Bluetooth BLE con interfaccia tipo UART.

Attraverso un’app tipo Bluetooth terminal è possibile:
- Inserire e disinserire l’allarme
- Consultare lo stato del sistema
- Modificare i parametri
- Avviare test
- Eseguire la diagnostica del sensore
- Configurare Wi-Fi e notifiche

La comunicazione BLE utilizza pairing protetto, autenticazione e PIN di accesso.

---

### Configurazione completa
Tutti i principali parametri sono configurabili dal menu setup:
- Rete Wi-Fi
- Password Wi-Fi
- Numero WhatsApp
- API key
- Ritardo di uscita
- Ritardo di ingresso
- Durata allarme
- PIN di sicurezza
- Nome Bluetooth
- Abilitazione WhatsApp
- Test sirena
- Test WhatsApp
- Secondo numero WhatsApp
- Seconda API key
- Inserimento automatico all’avvio
- Test connessione Wi-Fi
- Livello attivo del PIR
- Diagnostica PIR su relè
- Inversione uscita relè

Le impostazioni vengono conservate nella memoria EEPROM con controllo CRC, per ridurre il rischio di utilizzare dati corrotti.

---

### Inserimento automatico
La funzione di auto-inserimento permette di attivare automaticamente l’allarme all’avvio del dispositivo.

È utile, ad esempio, quando anzichè usare il bluetooth si preferisce attivare il sistema tramite un interruttore o una chiave nascosti; questo implica:
- Impostare tempo di uscita
- Impostare tepo di entrata

---

### Aggiornamento OTA
Quando viene attivata la modalità manutenzione, il firmware può essere aggiornato via Wi-Fi senza collegare fisicamente il dispositivo al computer.

L’aggiornamento OTA è protetto da autenticazione e consente di:
- Installare nuove versioni del firmware
- Correggere eventuali problemi
- Aggiungere nuove funzioni
- Effettuare manutenzione direttamente sul veicolo

---

### Affidabilità e sicurezza operativa
Il sistema include un watchdog hardware/software che controlla il corretto funzionamento del firmware e può riavviare il dispositivo in caso di blocco.

Il watchdog viene sospeso durante la configurazione manuale, evitando riavvii mentre l'utente sta lavorando nel menu, e viene riattivato al termine delle operazioni.

---

### Una piattaforma personalizzabile
Camper Alarm ESP32-C3 non è soltanto un semplice sensore con sirena: è una piattaforma configurabile per la sicurezza del veicolo.

Può essere adattata a:
- Camper
- Roulotte
- Van
- Rimorchi
- Piccoli locali tecnici
- Box e depositi
- Impianti di sicurezza personalizzati

La combinazione di sensori, relè, Bluetooth, Wi-Fi, notifiche WhatsApp, memoria permanente e aggiornamenti OTA offre una soluzione completa, flessibile e ampliabile.

---

### La sicurezza del tuo camper, sotto controllo
Con **Camper Alarm ESP32-C3** puoi sapere quando il sistema è attivo, ricevere una notifica in caso di intrusione, verificare l’impianto durante l’installazione e modificare la configurazione senza intervenire sul cablaggio.

Una soluzione compatta, intelligente e progettata per adattarsi alle esigenze reali di ogni installazione.
