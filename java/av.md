- se lucreaza cu diacritice (GUI si date)?
- excel: exista versiuni diferite de microsoft office
- care este doferenta intre Modulul Transfer FTP si Modulul de prelucrare date prin fisiere Excel?
- trebuie implementat mecanismul pt retrimite de fisiere si corectii
- au adrese IP fixe pt a restrictiona accesul la nivel de IP?
- productie: windows sau linux?
- cum anume preiau serviciile REST informatiile de la filiale?
    - preiau fisiere?
    - se acceseaza serviciul REST(POST) pentru fiecare informatie ce trebuie inserata?

Eu cred ca trebuie ca datele de la filiale sa se preia in forma bulk. 
- clientul FTP e foarte bun, sau 
- eventual un web service de tip SOAP, sau
- pur si simplu un form web cu file upload
Odata ajunse datele pe server ele vor fi prelucrate.

Pentru prelucrare exista un framework Spring Batch care te ajuta sa faci exact acest lucru: http://projects.spring.io/spring-batch/

Si pentru aplicatia web cu securitate se pot folosi frameworkurile http://projects.spring.io/spring-framework/ si http://projects.spring.io/spring-security/ 
iar pentru accesul la baza de date http://projects.spring.io/spring-data/ 



