# Piano di attivazione futura delle statistiche

Stato al 3 novembre 2026: **questa PR non autorizza né attiva nuova raccolta di dati**. Allinea l'informativa sulle pagine di condivisione al codice sorgente, senza modificare SDK, consensi o deploy.

## Stato verificato
- Firebase Analytics resta integrato nell'app ed è previsto come facoltativo, previo consenso (§3.12). Non dichiararlo rimosso senza intervenire nel codice e verificare le build.
- In `backend/api/share.js`, gli snippet Vercel Web Analytics e Speed Insights sono vuoti. **Verificare il deploy effettivo prima di pubblicare la nuova informativa**.
- Nel database Supabase non sono state individuate tabelle o colonne dedicate a visualizzazioni, clic o impression degli eventi.

## Checklist prima di introdurre statistiche proprietarie
1. Definire metriche, finalità e destinatari, inclusi eventuali report a pagamento per organizzatori.
2. Specificare dati trasmessi dal dispositivo, identificatori, deduplicazione, granularità e conservazione; preferire contatori aggregati e non comunicare dati individuali agli organizzatori.
3. Valutare la base giuridica e le regole ePrivacy con un professionista: **la monetizzazione non rientra automaticamente nell'esenzione per analytics tecnici**. L'aggregazione successiva non sana una raccolta iniziale illecita.
4. Aggiornare informativa e, ove necessario, registro dei trattamenti, gestione dei diritti e valutazione DPIA.
5. Se necessario il consenso, predisporre un opt-in preventivo, specifico e revocabile, testato su Android/iOS/web.
6. Verificare deploy, configurazioni effettive e dichiarazioni privacy degli store, mantenendo allineate le versioni italiana e inglese.

Questo documento è una checklist operativa, non un parere legale.
