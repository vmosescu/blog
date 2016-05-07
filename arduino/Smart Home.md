- bestbuy:
    - samsung: 40 usd: multipurpose, water, motion
    - securifi: 30 usd: door, motion (40)
- sparkfun

# Senzori
- La usa deschisa cand circuitul e deschis nu se stie exact *floating*
- trebuie folosit *pull-up resistor*

# Wi-Fi

S-a decis folosirea XBee
- foloseste protocolul ZigBee
- nu prea exista senzori gata de cumparat in Europa (mai trebuie cautat); in USA am gasit o gramada
- trebuie avut in vedere consumul mare de curent: programare stufoasa pt economia de energie (Arduino+XBee)
- cap 6 din Arduino Wireless
- 

# Home Controller
- XBee Coordinator
- Raspberry PI
- conexiuni posibile
    - XBee - Arduino WiFi Gateway - Arduino Ethernet - Paspbery PI
    - XBee - Arduino WiFi Gateway - Raspbery Pi (Phyton)
    - Xbee - Raspbery Pi


# OpenHAB

Usa deschisa
Problema e cum afisam istoricul
1. Prin grafice: nu e destul de vizibil
  OpenHAB poate afisa grafice cu rrd4j
  Se pot crea poze pe server (Sencha Charts or Google Chart Tool) si apoi afisate
  
2. Text
  OpenHAB nu prea poate afisa text
  Textul sa fie creat de o aplicatie web
  site-ul web sa fie afisat in OpenHab printr-un sitemap de tip webview sau 
  se poate accesa direct site-ul
  
Persistenta
MangoDB: pe raspberry pi se instaleaza mai greu
  -> trebuie totusi incercat; se preteaza pt IOT
mySQL: tu creezi db, openHAB creaza automat tabelele (la prima salvare a unui item)
tabele sunt predefinite: PK de tip time, si o alta coloana in functie de item pt valoare

REST
default este instalat REST pentru interogarea configuratiei si altele /rest
nu am putut instala modulul REST de interogare a persistentei: 
  cica trebuie instalat HABmin: o aplicatie web pt configurare si altele
  cica ar trebuie sa mearga si /rest/persistence/ dupa instalare, dar nu merge
