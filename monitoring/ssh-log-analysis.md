# Report Analisi Log: Tentativi di Intrusion SSH

## Panoramica
Durante il monitoraggio del file `/var/log/auth.log`, sono stati rilevati molteplici tentativi di connessione non autorizzati provenienti da diversi indirizzi IP.

## Evidenze
Il sistema ha correttamente respinto i tentativi:
- **Tentativi di connessione root**: Diversi IP hanno tentato l'autenticazione come root.
- **Tentativi su utenze inesistenti**: È stato rilevato un tentativo per l'utente 'admin' (es. IP 2.57.121.112).

## Conclusione
Le configurazioni di sicurezza (disabilitazione password, restrizione root, chiavi SSH) impediscono con successo l'accesso non autorizzato. Il server non presenta vulnerabilità a questi tentativi di brute force standard.

## Log (Estratto)
```text
2026-05-28T12:14:53.202458+00:00 il-mio-server sshd[119013]: Invalid user admin from 2.57.121.112 port 39856
2026-05-28T12:14:53.343391+00:00 il-mio-server sshd[119013]: Disconnected from invalid user admin 2.57.121.112 port 39856 [preauth]
