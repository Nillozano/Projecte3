## 1. Requeriments d'Infraestructura Inicial
Primer de tot hem de configurar la màquina server (Server Hostname) posem aquesta comanda per configurar l’arxiu.

![](img/01.png)

Ara posem com a nom del host: server.innotechXX.test         XX=número de llista

![](img/02.png)

Mirem que s’hagi guardat el canvi.

![](img/03.png)

Seguidament configurem la xarxa, el adaptador 1 com a NAT (el predeterminat).

![](img/04.png)

I el segon adaptador en “Adaptador de només l’amfitrió” perque només pugui interactuar el client virtual amb la màquina física.

![](img/05.png)

Ara activarem el segon adaptador.

![](img/06.png)

![](img/07.png)

Ho apliquem.

![](img/08.png)

Mirem que las IP’s estiguin ben configuradas

![](img/09.png)

## 2. Tasques d'Implementació i Configuració del Servidor LDAP
### 2.1. Instal·lació i Configuració Base d'OpenLDAP
Seguidament instal·lem el servei OpenLDAP

![](img/10.png)

Posem la contrasenya “usuari”.

![](img/11.png)

![](img/12.png)

Comproven que s’hagi instalat amb status.

![](img/13.png)

Seguidament posem aquesta comanda per veure les dades del directori “LDAP”.

![](img/14.png)

Ara per configurar la base de dades posem aquesta comanda, tot per reconfigurar el paquet.

![](img/15.png)

Després diu “no es crearà la configuració ni la base de dades inicial si habilitem aquesta
opció” i li posem que no volem ometre la configuració del servidor OpenLDAP.

![](img/16.png)

Li posem el nom de domini DNS (el que ja et ve predeterminat).

![](img/17.png)

Ara al nom de l’organització (també el predeterminat).

![](img/18.png)

I posem la contrasenya d’administrador: p@ssw0rd

![](img/19.png)

![](img/20.png)

Seguidament posem que s’elimini el paquet, és a dir que s’elimini la BD que hem creat.

![](img/21.png)

I movem la informació del directori a una carpeta backup.

![](img/22.png)

![](img/23.png)

Seguidament comprovem que tot el que hem configurat en els passos anterios s’hagi guardat.

![](img/24.png)

Ara posem aquesta comanda per editar el ou.ldif i el configurem de la següent forma.

![](img/25.png)

![](img/26.png)

Després agregarem l’arxiu al directori.

![](img/27.png)

I fem una consulta amb la comanda ldapsearch mostrant totes les OUs creades al
directori.

![](img/28.png)

### 3.2. Gestió i Administració (LAM)
Seguidament ens instal·larem el gestor d’usuaris ldap.

![](img/29.png)

![](img/30.png)

Després per obrir la web haurem de mirar la nostra ip per entrar a la web que ens pertoca.

![](img/31.png)

Seguidament, per entrar a la web posem la nostra ip i després un “/lam”.

![](img/32.png)

Abans d'iniciar la sessió el primer pas de la web serà configurar el gestor. Entrant a edita els fitxers del servidor.

![](img/33.png)

Entrem com a lam.

![](img/34.png)

I començem la nostra configuració tal i com mostra les imatges.

![](img/35.png)

![](img/36.png)

En aquì posem que els nous usuaris ess posin al OU users i els grups igual.

![](img/37.png)

Un cop la configuració ja acabada podrem iniciar la sessió amb el admin i la contrasenya que en el principi de la guia posem (p@ssw0rd).

![](img/38.png)

Ara crearem dos grups, el tech i el manager.

![](img/39.png)

![](img/40.png)

![](img/41.png)

Seguidament, un cop creat els grups, creem un usuari per cada grup, tech01 i manager01.

![](img/42.png)

![](img/43.png)

![](img/44.png)

![](img/45.png)

![](img/46.png)

![](img/47.png)

Un cop ja tot creat mirem que s’hagi creat correctament, tant els grups com els usuaris.

![](img/48.png)

![](img/49.png)

## 4. Integració de Client
En un ubuntu configurarem la màquina del client. Primer de tot configurarem la xarxa perquè la interfície en comuniqui en host-only amb el servidor.

![](img/50.png)

![](img/51.png)

Per verificar que ho hàgim configurat bé fem ip a.

![](img/52.png)

Seguidament fora de la màquina farem una instantanea.

![](img/53.png)

Després farem les actualitzacions.

![](img/54.png)

Ara configurarem l’arxiu hosts

![](img/55.png)

Editant en la segona i tercera línia el nom i la ip (la mateixa que hem mirat abans amb ip a).

![](img/56.png)

Continuant editarem l’arxiu hostname

![](img/57.png)

L’hi posem el nom que hem configurat abans.

![](img/58.png)

I mirem que s’hagi canviat les dos configuracions.

![](img/59.png)

![](img/60.png)
