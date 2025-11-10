# Fase Pràctica: Diagnosi de Noms (Auditoria amb CLI)

Heu de demostrar l'ús de les principals utilitats de diagnosi DNS en els diferents sistemes operatius que utilitza el client (Linux/macOS i Windows).

Per a cada eina, executeu les comandes indicades a continuació contra el domini que s’indiqui explícitament i captureu/analitzeu els resultats.

Per fer aquesta demostració, caldrà usar un equip Zorin amb dues interfícies:
- La primera en NAT
- La segona en adaptador pont amb la IP correctament configurada segons indicacions dels vostres responsables.

---

## A. Diagnosi Avançada amb `dig` (Linux / macOS)

### Comanda 1: Consulta Bàsica de Registre A
```bash
dig xtec.cat A
```
**Anàlisi**: Identifica la IP de resposta, el valor TTL i el servidor que ha respost a la consulta.

### Comanda 2: Consulta de Servidors de Noms (NS)
```bash
dig tecnocampus.cat NS
```
**Anàlisi**: Quins són els servidors de noms autoritatius per a aquest domini?

### Comanda 3: Consulta Detallada SOA
```bash
dig escolapia.cat SOA
```
**Anàlisi**: Quina és la informació del correu de l'administrador i el número de sèrie del domini?

### Comanda 4: Consulta resolució inversa
```bash
dig -x 147.83.2.135
```
**Anàlisi**: Quina informació sobre els registres s’obté?

---

## Comprovació de Resolució amb `nslookup` (Multiplataforma)

L’eina `nslookup` es troba a pràcticament qualsevol sistema operatiu. Es pot usar de forma similar a `dig`, incloent l’argument, o si s’executa `nslookup` sense arguments, entra en el mode interactiu amb un prompt (`>`). Serà aquest mode el que explorareu.

### Comandes bàsiques en mode interactiu:
- `set type=`: per indicar el tipus de consulta (A, AAAA, MX, NS, SOA, TXT, ALL)
- `server IP`: per indicar la IP o nom del servidor de noms
- `exit`: per sortir del mode interactiu

### Comanda 1: Consulta Bàsica no Autoritativa
```text
> set type=A
> tecnocampus.cat
```
**Anàlisi**: Per què indica que la resposta és no autoritativa?

### Comanda 2: Consultes autoritatives
```text
> server [IP del primer servidor de noms obtingut]
> set type=A
> tecnocampus.cat
```
**Anàlisi**: Quines diferències s’observen a la resposta obtinguda amb la comanda 1?

---

## Resolucions locals

Es vol comprovar el funcionament de la resolució local, útil per entorns de xarxa local on no es disposa de servidor de noms propi i que evita haver d’accedir a equips o recursos per la seva IP.

---

## Activitat de la Fase Pràctica

Crear un document `guia.md` amb:
- Resultats i anàlisi de les **6 comandes anteriors**
- **Captures de pantalla** de les execucions
- **Explicacions relacionades**
- **Proves de resolució local**

---
# Solució:
- [Solució](Solució.md)
- [Vídeo](Video.md)
