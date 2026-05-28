# 01 - Configurazione Iniziale Server

Questa fase riguarda il provisioning iniziale e la configurazione dell'utente amministrativo su un'istanza Ubuntu.

## Creazione Utente con privilegi Sudo
Per motivi di sicurezza, non operiamo direttamente come `root`. Abbiamo creato un utente dedicato:

```bash
# Creazione dell'utente
sudo adduser nomeutente

# Assegnazione dei privilegi amministrativi
sudo usermod -aG sudo nomeutente
