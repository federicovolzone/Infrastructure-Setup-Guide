# 02 - SSH Hardening

Questa sezione documenta la messa in sicurezza dell'accesso remoto al server, disabilitando l'autenticazione tramite password a favore di quella tramite chiavi crittografiche (Public/Private Key).

## Generazione delle chiavi (Lato Client)
Per accedere in modo sicuro, abbiamo generato una coppia di chiavi sul computer locale:

```bash
# Generazione della coppia di chiavi
ssh-keygen -t ed25519 -C "tua_email@esempio.com"

# Trasferimento della chiave pubblica sul server
ssh-copy-id -i ~/.ssh/id_ed25519.pub nomeutente@ip_del_server
Configurazione del servizio SSH (Lato Server)
Abbiamo modificato il file /etc/ssh/sshd_config per applicare restrizioni severe:

Bash
# Modifica del file di configurazione
sudo nano /etc/ssh/sshd_config

# Parametri implementati:
# Port <numero_porta>            # Modificata per evitare scansioni automatiche
# PermitRootLogin no             # Accesso root disabilitato
# PasswordAuthentication no      # Autenticazione password disabilitata

# Riavvio del servizio per applicare le modifiche
sudo systemctl restart ssh
Risultato
Il server accetta ora esclusivamente connessioni crittografiche autenticate, eliminando la vulnerabilità verso attacchi di tipo brute force basati su password.
