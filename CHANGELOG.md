# Changelog - Spin2Call ☎️

Tutte le modifiche del firmware, dell'app e dell'hardware di Spin2Call, il telefono a disco Bluetooth.

---

## [0.2.4] - 2026-10-21
### Telefono
- **Lo step-up dei 35 V non scalda più.** Lo accende un relè solo quando la campana suona, e lo spegne pochi secondi dopo. Serve il relè sul GPIO18 (vedi lo schema dei collegamenti).
- **La tua voce più calda.** Il filtro del microfono taglia sotto i 150 Hz invece che sotto i 300: passano i bassi della voce.

### Hardware
- Modulo relè per lo step-up, e un diodo con un condensatore da 1000 µF che separano l'alimentazione dell'ESP32: quando lo step-up si accende, l'ESP32 non si riavvia più.

---

## [0.2.3] - 2026-10-21
### Telefono
- **Voce dell'altro limpida.** Il limitatore del volume nel ricevitore era troppo lento per il processore e con la voce in arrivo saltava un campione su dieci: voce grave e distorta per te, disturbi per l'altro. Ora è una formula veloce, e il volume di base è dimezzato (il cellulare manda la voce già quasi al massimo). Se ti sembra bassa, alza il volume dall'app.
- **Niente più eco per chi ti ascolta**, e niente scarica quando smette di parlare: mentre parla lui il microfono resta abbassato, e per un quarto di secondo dopo.
- **Niente scariche nelle pause**: un filtro toglie i disturbi brevi sul filo del microfono.
- **Squillo di libero nella cornetta** quando la chiamata parte dal cellulare con la cornetta alzata, invece del tono di centrale.
- Processore a 240 MHz per avere margine sull'audio.

---

## [0.2.2] - 2026-10-21
### Telefono
- **Meno eco per chi ti ascolta.** Quando l'altro parla, il microfono della cornetta viene abbassato a meno che tu non parli più forte di lui: la sua voce, che dal ricevitore rientrava nel microfono, non gli torna più indietro.

---

## [0.2.1] - 2026-10-20
### Telefono
- **Voce più pulita in chiamata.** Chi ascolta non sente più il gracchiare dovuto ai pacchetti audio incompleti: quando il telefono resta indietro di qualche campione, ora lo recupera invece di riempire il buco di silenzio.
- **Meno fruscio nelle pause.** Il filtro che abbassa il microfono quando non parli ora si chiude davvero sul rumore di fondo, e lo abbassa di più (26 dB invece di 16).

---

## [0.2.0] - 2026-10-20
### Telefono
- **Il modem 56k.** Ogni tanto, alzando la cornetta, invece del tono di centrale si sente l'handshake di un vecchio modem: la composizione del numero, il tono di risposta a 2100 Hz, i fruscii e i bip dei due modem che si mettono d'accordo. Dura circa 18 secondi; appena giri il disco si interrompe, e finito il suono torna il tono di centrale.
- **Numero di servizio 56**: componendolo parte subito, per riascoltarlo quando vuoi.

### App
- Nuova opzione **Rumore del modem 56k** nelle impostazioni: mai, ogni tanto (una volta su dieci), spesso (una su tre), sempre. Di serie: ogni tanto.

---

## [0.1.0] - 2026-10-20
### Telefono
- **Prima versione**: telefono a disco SIP (Siemens S62 "Bigrigio") collegato al cellulare come vivavoce Bluetooth. Si compone col disco, squilla la campanella originale, si parla dalla cornetta originale.
- **Numeri brevi**: una sola cifra da 1 a 9 chiama il numero salvato nella rubrica; lo 0 da solo apre l'assistente vocale del cellulare.
- **Aggiornamenti via Bluetooth**: il firmware si aggiorna dall'app; se la versione nuova non parte, il telefono torna da solo alla precedente.
- Tono di centrale e di occupato con le cadenze SIP, soppressione dell'eco e del rumore di fondo durante la chiamata.

### App
- **App Spin2Call per Android**: stato del telefono, rubrica dei numeri brevi (anche dai contatti), volume del ricevitore, sensibilità del microfono, suoneria (attiva, cadenza Italia/USA/UK, prova), attesa prima della chiamata, tono di centrale.
- Aggiornamento del firmware del telefono e dell'app stessa da GitHub.
