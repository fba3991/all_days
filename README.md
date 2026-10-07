# All Days Budget

App web in italiano per gestire un budget mensile, registrare entrate e spese e visualizzare le spese per categoria. Layout adattato a desktop e telefono.

## Sviluppo

Richiede Node.js 24 e npm 11.

```sh
npm ci --cache /tmp/all-days-npm-cache
npm run dev -- --port 5173 --strictPort
```

## Verifiche

```sh
npm run build
npm test
```

I test usano Chromium in `/usr/bin/chromium` nell’ambiente cloud. Verificano calcoli, salvataggio, separazione dei mesi, eliminazione, layout mobile e visualizzazione sicura delle descrizioni.

I dati rimangono nel localStorage di questo browser: non sono sincronizzati né salvati su un account. Cancellando i dati del browser si eliminano i movimenti. Il budget è il limite di spesa scelto per il mese; il saldo è la differenza tra entrate e spese registrate, senza saldo iniziale.
