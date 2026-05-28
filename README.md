# Infrastructure-Setup-Guide

Questo progetto documenta la configurazione, l'hardening e il monitoraggio di un'infrastruttura server Linux (Ubuntu) in ambiente cloud. Lo scopo è implementare standard di sicurezza di produzione, garantendo resilienza contro tentativi di accesso non autorizzati.

## Struttura del Progetto

- **[docs/](docs/)**: Documentazione tecnica delle fasi di provisioning, hardening SSH e configurazione firewall (UFW).
- **[monitoring/](monitoring/)**: Analisi attiva e reportistica sui tentativi di intrusione rilevati (analisi log di sistema).

## Obiettivi di Sicurezza
- Riduzione della superficie di attacco.
- Implementazione di autenticazione basata su chiavi crittografiche (Public Key Authentication).
- Monitoraggio continuo dei log di sistema per identificare pattern di brute force.

---
*Progetto sviluppato come parte del percorso di specializzazione in Cybersecurity.*
