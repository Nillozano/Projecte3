## Fase Pràctica: Diagnosi de Noms (Auditoria amb CLI)
Heu de demostrar l'ús de les principals utilitats de diagnosi DNS en els diferents sistemes operatius que utilitza el client (Linux/macOS i Windows).
Per a cada eina, executeu les comandes indicades a continuació contra el domini que s’indiqui explícitament i captureu/analitzeu els resultats.
Per fer aquest demostració, caldrà usar un equip Zorin amb dues interfícies, la primera en NAT i la segona en adaptador pont amb la IP correctament configurada segons indicacions dels vostres responsables.
[]()
### A. Diagnosi Avançada amb dig (Linux / macOS)
#### Comanda 1: Consulta Bàsica de Registre A
- Executa dig xtec.cat A
- Anàlisi: Identifica la IP de resposta, el valor TTL i el servidor que ha respost a la consulta.
- Quan es consulta el domini xtec.cat, es rep la IP 83.247.151.214, amb un TTL de 753 segons. El servidor que respon és 127.0.0.53, que gestiona les peticions DNS localment.
[]()
#### Comanda 2: Consulta de Servidors de Noms (NS)
- Executa dig tecnocampus.cat NS
- Anàlisi: Quins són els servidors de noms autoritatius per a aquest domini?
- Els servidors de noms autoritatius del domini tecnocampus.cat són: ns-1689.awsdns-19.co.uk, ns-535.awsdns-02.net, ns-1071.awsdns-05.org i ns-130.awsdns-16.com.
[]()
[]()
#### Comanda 3: Consulta Detallada SOA
- Executa dig escolapia.cat SOA
- Anàlisi: Quina és la informació del correu de l'administrador i el número de sèrie del domini?
- El correu de l’administrador del domini escolpia.cat és dnsmaster@comenic.org i el número de sèrie associat al registre SOA és 2510301532, que indica la versió actual de la zona DNS.
[]()
#### Comanda 4: Consulta resolució inversa
- Executa comanda dig -x 147.83.2.135
- Anàlisi: Quina informació sobre els registres s’obté?
- L’adreça IP 147.83.2.135 té diversos registres PTR que apunten a dominis relacionats amb la Universitat Politècnica de Catalunya (UPC), com upc.edu, upc.cat, masters.upc.edu, saladepremsa.upc.edu, barcelonatech.upc.edu i altres, indicant que aquesta IP està associada a serveis i subdominis de la UPC.
[]()
[]()
#### Comprovació de Resolució amb nslookup (Multiplataforma)
L’eina nslookup es troba a pràcticament a qualsevol sistema operatiu. Es pot usar de forma similar a dig incloent l’argument o si s’executa nslookup sense arguments, entrar en el mode interactiu, us apareix un prompt (>). Serà aquest mode el que explorareu . 
[]()
El mode és força senzill, bàsicament hi ha tres comandes a usar:
- set type= per indicar el tipus de consulta: A, AAA, MX, NS, SOA, TXT o ALL.
- server IP on IP és la IP del servidor de noms al que es vol fer la consulta, també es pot indicar el nom del servidor enlloc de la IP, per exemple, server a9-66.akam.net.
- exit que serveix per sortir de la comanda.
#### Comanda 1: Consulta Bàsica no Autoritativa
- Seleccionar type=A i com a domini de consulta tecnocampus.cat
- Anàlisi: Per què indica que la resposta és no autoritativa?
- La resposta és no autoritativa perquè prové d’un servidor DNS recursiu (en aquest cas, el local 127.0.0.53) que ha obtingut la informació d’una memòria cau o d’un altre servidor, i no directament dels servidors autoritatius del domini.
[]()
#### Comanda 2: Consultes autoritatives
- Escriure server IP i escriure la IP del primer servidor de noms del domini tecnocampus.cat que s’ha obtingut d’una consulta anterior. A continuació, indiqueu que voleu consultar registres de tipus A i del domini tecnocampus.cat
- Anàlisi: Quines diferències s’observen a la resposta obtinguda amb la comanda 1?
- La primera no era autoritativa i aquesta si que ho és.
[]()
[]()
[]()
#### Resolucions locals
Finalment es vol comprovar el funcionament de la resolució local, útil per entorns de xarxa local on no es disposa de servidor de noms propi i que evita haver d’accedir a equips o recursos per la seva IP.
[]()
(És l’Anthony)
