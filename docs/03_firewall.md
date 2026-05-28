# 03 - Configurazione Firewall (UFW)

Questa sezione documenta la configurazione del firewall `ufw` (Uncomplicated Firewall) per limitare la superficie di esposizione del server, consentendo solo il traffico strettamente necessario.

## Configurazione delle regole di filtraggio
Abbiamo adottato una politica di "default deny" per il traffico in entrata, garantendo la chiusura di tutte le porte non esplicitamente autorizzate:

```bash
# Definizione delle policy di default
sudo ufw default deny incoming
sudo ufw default allow outgoing

# Apertura della porta SSH personalizzata
# Sostituire <porta> con il numero di porta configurato in precedenza
sudo ufw allow <porta>/tcp

# Attivazione del firewall
sudo ufw enable
Verifica dello stato
Per confermare che le regole siano attive e monitorare il traffico filtrato:

Bash
# Visualizzazione dello stato attuale del firewall
sudo ufw status verbose
Obiettivo
L'obiettivo è limitare drasticamente gli accessi non autorizzati al sistema, assicurando che il server risponda esclusivamente alle richieste necessarie, migliorando la resilienza complessiva dell'infrastruttura.
