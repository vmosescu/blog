- XBee Explorer USB: configureaza XBee prin conectare la PC prin USB (5v->3.3v)
- 

1. Se configureaza XBee cu XCTU
  - Coordinator API: cel ce primeste, langa Raspberry pi
  - Router API: cel care trimite mesaje de la senzor

#### Comunicare cu Arduino
- hardware serial port (UART): DIN/DOUT se leaga la TX/RX
  - trebuie vazut cum se foloseste libraria
  - nu poate fi utilizat cand Arduino e legat la PC deoarece se foloseste acelasi UART
- software serial port: DIN/DOUT se leaga la 2 pini digitali
  - se poate folosi libraria AltSoftSerial care foloseste pinii 8/9
  - shield-ul XBee are un switch care conecteaza pinii DIN/DOUT la UART sau la pinii 2/3
  - se poate folosi urmatoarea configuratie pt ca Arduino sa fie legat la PC si in acelasi timp la XBee:
    - libraria AltSoftSerial 
    - switch shield pt pinii DIN/DOUT la pinii 2/3
    - se leaga pinii 2/3 cu 8/9

#### Sleep
- XBee consuma mult; pt asta se trece pe sleep
- doar in configuratia End Device poate trece pe sleep
  - Router API cu SM>0
  - End Device API 
- sleep modes:
  - pin sleep (SM=1)
  - cycle sleep (SM=4)
  - cycle + pin (SM=5)
- cand se utilizeaza ca si end device sa fim atenti la configurarea parintelui (Router sau Coordinator) pt SP si SN
