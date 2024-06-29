# Wi-Fi-


avvia scheda di rete in monitor mode
```
erpressa@kali:~# sudo airmon-ng start wlan0
```

avvia airodump-ng per scansionare
```
sudo airodump-ng wlan0mon 
```
premere spazio per fe copiare bssid
oppure ctrl + c per terminare 
```

sudo airodump-ng --bssid FF:FF:FF:FF:FF:FF -c 1 -w /home/kali/handshake.cap wlan0mon
```
esempio sudo airodump-ng --<BSSID> -c <CANALE> -w <PERCORSO-FILE>  <INTERFACCIA>
