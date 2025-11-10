# Gestió Segura de Contrasenyes a EverPia

## Introducció i Justificació

L'ús de contrasenyes febles o reutilitzades representa un risc crític per a la seguretat de l'empresa. Aquestes pràctiques poden exposar els sistemes corporatius a diversos tipus d'atacs:

- **Atacs de diccionari**
- **Credential stuffing**
- **Phishing i enginyeria social**

Un incident de seguretat recent ha posat de manifest aquesta vulnerabilitat, subratllant la necessitat d'adoptar mesures proactives.

### La funció d’un gestor de contrasenyes

Un gestor de contrasenyes pot mitigar aquests riscos mitjançant:

- Generació automàtica de contrasenyes robustes i úniques
- Emmagatzematge segur amb xifratge
- Accés centralitzat i controlat a les credencials

---

## Comparativa Tècnica

### Bitwarden (Alternativa Online / Núvol)

- **Sincronització:** Automàtica entre dispositius
- **Model de seguretat:** Xifratge end-to-end (AES-256)
- **Accés:** Web, mòbil, escriptori, extensions de navegador
- **Cost:** Model freemium
- **Auditories:** Regulars i públiques

### KeePassXC (Alternativa Offline / Escriptori)

- **Emmagatzematge:** Local (fitxer KDBX)
- **Model de seguretat:** Xifratge local (AES/Rijndael)
- **Accés:** Escriptori (Windows, macOS, Linux)
- **Sincronització:** Manual (cal copiar l’arxiu)
- **Model de llicència:** Codi obert complet
- **Auditories:** Comunitàries, menys freqüents

---

## Taula Comparativa

| Característica         | Bitwarden (Online)                          | KeePassXC (Offline)                          |
|------------------------|---------------------------------------------|----------------------------------------------|
| **Model de seguretat** | Xifratge end-to-end (AES-256)               | Xifratge local (AES/Rijndael)                |
| **Emmagatzematge**     | Núvol (Bitwarden Cloud o servidors propis)  | Local (fitxer KDBX en disc o USB)            |
| **Accés multiplataforma** | Web, mòbil, escriptori, extensions navegador | Escriptori (Windows, macOS, Linux)           |
| **Sincronització**     | Automàtica                                  | Manual                                       |
| **Model de llicència** | Freemium                                    | Codi obert complet                           |
| **Auditories**         | Regulars i públiques                        | Comunitàries                                 |
| **Facilitat d’ús**     | Alta (interfície intuïtiva)                 | Mitjana (més tècnic)                         |
| **Portabilitat**       | Alta (accés des de qualsevol lloc)          | Alta (fitxer portàtil, però sense sincronització) |
| **Dependència d’Internet** | Sí                                       | No                                           |

---

## Avantatges i Inconvenients

### Bitwarden

**Avantatges:**
- Sincronització automàtica
- Accés des de qualsevol dispositiu
- Interfície moderna i fàcil d’utilitzar
- Auditories externes de seguretat

**Inconvenients:**
- Dependència d’Internet
- Potencial risc si el servidor és compromès

### KeePassXC

**Avantatges:**
- Control total de les dades
- Ideal per entorns amb requisits de seguretat estrictes
- Codi obert i gratuït

**Inconvenients:**
- No hi ha sincronització automàtica
- Més complex d’utilitzar
- Risc de pèrdua de dades si no es fa còpia de seguretat

---

## Recomanació

Es recomana implementar **Bitwarden** com a gestor de contrasenyes per al personal tècnic d’**EverPia**. La seva facilitat d’ús, capacitat de sincronització, model de seguretat robust i auditories externes el fan ideal per a un entorn corporatiu que necessita una solució escalable, segura i fàcil de desplegar.


## Torna a l'anucnciat
[Anunciat](Readme.md)
