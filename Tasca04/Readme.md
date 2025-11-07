# Implementació d'OpenLDAP per a Innovatech

## Descripció General
Innovatech és una start-up tecnològica emergent que està experimentant un ràpid creixement i es troba en una situació de caos a l'hora de gestionar els seus usuaris i accessos. Actualment, cada servei intern (servidor de fitxers, wiki de documentació, etc.) utilitza la seva pròpia base de dades d'usuaris i contrasenyes, mentre que els ordinadors clients utilitzen autenticació local. Això crea diversos problemes crítics per a l'empresa:

- **Ineficiència Operativa:** La creació i eliminació de comptes en múltiples sistemes cada cop que s'incorpora o marxa un empleat resulta en un procés lent i propens a errors.
- **Risc de Seguretat:** Els usuaris sovint reutilitzen les contrasenyes per diversos serveis per evitar l’oblit, augmentant el risc de vulnerabilitats de seguretat.
- **Manca d'Escalabilitat:** A mesura que Innovatech creix i afegeix més serveis, la gestió d'usuaris es fa cada vegada més insostenible.

El CEO d'Innovatech ha contactat amb **EverPia** per implementar una solució d'autenticació centralitzada. La solució proposada és utilitzar **OpenLDAP** (Lightweight Directory Access Protocol), una solució robusta i de codi obert, que s’adapta perfectament a l'entorn de **GNU/Linux** de l'empresa.

## Objectiu de la Tasca
La tasca consisteix en implementar el servei **OpenLDAP** en un servidor Linux, de manera que centralitzi l'autenticació i gestió d'usuaris a tota l'empresa. Els requisits específics inclouen:

1. **Instal·lació del servei OpenLDAP.**
2. **Configuració del domini base i creació de la jerarquia d'unitats organitzatives.**
3. **Integració d'usuaris i grups al directori OpenLDAP per a la seva utilització en serveis de xarxa.**
4. **Configuració d'un client per utilitzar el directori OpenLDAP per autenticar els usuaris.**

Amb aquesta solució, Innovatech aconseguirà una gestió d'usuaris centralitzada, millorant l'eficiència operativa, la seguretat i l'escalabilitat dels seus serveis.

## Passos de la Implementació

### 1. Instal·lació d'OpenLDAP
- Instal·lació del servei **OpenLDAP** al servidor Linux.
- Configuració inicial del directori per permetre la integració amb altres serveis.

### 2. Configuració del Domini Base
- Definició del **domini base** i les unitats organitzatives (OUs) necessàries per organitzar els usuaris i grups de manera eficaç.

### 3. Creació de la Jerarquia d'Unitats Organitzatives
- Creació d'unitats organitzatives (OUs) per a diferents departaments i grups dins de l'empresa.

### 4. Integració d'Usuaris i Grups
- Creació d'usuaris i grups a OpenLDAP per a gestionar les autentificacions dels diferents serveis interns (servidor de fitxers, wiki, etc.).

### 5. Configuració del Client per Autenticar-se a OpenLDAP
- Configuració d'un client per utilitzar **OpenLDAP** com a sistema d'autenticació centralitzat, permetent la gestió unificada d'usuaris.

## Materials de Classe
Els següents documents es proporcionen per ajudar a completar aquesta tasca:

- **[UD04.AA1 Serveis de Directori](https://moodle.url)**
- **[UD04.AA2 Instal·lació OpenLDAP](https://moodle.url)**
- **[UD04.AA3 Configuració del directori](https://moodle.url)**
- **[UD04.AA5 Agregar client al directori](https://moodle.url)**

## Requisits Tècnics
La solució es basarà en una instal·lació de **OpenLDAP** en un servidor Linux que formi part de la infraestructura de la companyia. Tots els ordinadors clients utilitzaran **GNU/Linux** i seran configurats per autenticar-se a través d'OpenLDAP.

## Conclusió
Amb aquesta implementació, Innovatech aconseguirà un sistema d'autenticació centralitzada que millorarà la seguretat i l'eficiència operativa de l'empresa, a més de permetre una gestió escalable dels usuaris i accessos a mesura que l'empresa creixi.


