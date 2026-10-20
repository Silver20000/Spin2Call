# Changelog - Spin2Call ☎️

Tutte le modifiche del firmware, dell'app e dell'hardware di Spin2Call, il telefono a disco Bluetooth.

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
