# Tasca 03: Gestió d'Emmagatzematge amb LVM (Linux) i Espais d'Emmagatzematge (Windows)

## Descripció General
Aquesta tasca té com a objectiu implementar i demostrar la utilitat del *Logical Volume Manager* (LVM) en Linux (Zorin OS) i els *Storage Spaces* en Windows 11. Es realitzaran dues parts independents, una per a cada sistema operatiu, que demostraran les funcionalitats de cada tecnologia en relació a la gestió d'espais d'emmagatzematge, alta disponibilitat i escalabilitat.

## Contingut
1. **Part Linux: LVM amb Zorin OS**
   - Implementació de grups de volums, volum lògic, alta disponibilitat, instantànies i ampliació de volums.
2. **Part Windows: Espais d'Emmagatzematge (Storage Spaces)**
   - Creació de *Storage Pools* i demostració de diferents configuracions de resiliència i gestió de discos.

## Part 1: Linux - LVM amb Zorin OS

### Requisits de la Implementació i Demostració:

1. **Configuració Inicial:**
   - Crear un grup de volums (VG) i un volum lògic (LV) utilitzant un mínim de dos discs durs simulats de 10 GB cada un.
   - El volum ha d'estar formatat i muntat automàticament al sistema mitjançant l'edició de l'arxiu `/etc/fstab`.

2. **Alta Disponibilitat:**
   - Implementar la configuració d’un mirall (lvm_mirror) per protegir la informació davant la fallada d'un disc.

3. **Instantànies (Snapshots):**
   - Afegir dos discos de 10 GB al grup de volums.
   - Crear un volum (lvm_dades) amb el primer disc afegit, formatar-lo i muntar-lo.
   - Afegir arxius al volum (per exemple, imatges d'Internet).
   - Utilitzar el segon disc per crear un snapshot (`lv_snapshot`) i documentar com restaurar-lo en cas de dany en el volum original.

4. **Escalabilitat:**
   - Demostrar el procés d'ampliació, utilitzant l'espai lliure dins del grup de volums per ampliar el volum `lv_dades`.

## Part 2: Windows - Espais d'Emmagatzematge (Storage Spaces)

### Requisits de la Implementació i Demostració:

1. **Configuració Inicial:**
   - Crear un *Storage Pool* amb tres discs de 10 GB (simulats).

2. **Estudi de Configuracions:**
   - **Resiliència de Mirall (Mirroring):** Utilitzar dos dels discs per crear un Espai d'Emmagatzematge amb alta disponibilitat.
   - **Resiliència de Paritat (Parity):** Explicar l'eficiència d'espai en comparació amb el mirall, utilitzant els tres discs.
   - **Resiliència de Mirall Triple:** Afegir tants discos de 10 GB com sigui necessari.

3. **Demostració de la Gestió:**
   - Mostrar com es visualitza l'estat dels discos i del *pool* des de la consola de gestió de Windows i simular la facilitat de manteniment.

## Com Treballarem i Què Lliurarem

El treball es realitzarà en grups. Cada grup es dividirà en dues parelles, una responsable de la part de Linux amb LVM i l'altra de la part de Windows amb *Storage Spaces*.

### Fases de la Tasca:

1. **Preparació Individual:**
   - Cada membre del grup haurà de preparar un guió detallat de la tasca, cercant comandes i consultant enllaços de documentació.
   
2. **Realització de la Demostració:**
   - Cada parella serà responsable de realitzar la demostració pràctica del sistema assignat (LVM o Storage Spaces).

3. **Revisió i Documentació:**
   - Un cop finalitzada la demostració, el grup revisarà la documentació generada i cada membre l'uploadarà al seu repositori.
   
### Documentació:
La documentació dels dos casos es realitzarà en format Markdown i s'inclourà dins una carpeta anomenada `tasca03` al projecte. L'arxiu `README.md` de la carpeta ha de contenir:
- Descripció general de la tasca.
- Enllaços a la documentació de cada part (LVM i Storage Spaces).

La nota de la tasca és conjunta per tot el grup, així que és important organitzar-se bé i mantenir una bona comunicació interna.

### Presentació Final:
Després de completar la tasca, haureu de presentar les conclusions del treball en una presentació conjunta davant del client.

## Material de Classe
- [LVM Linux](https://moodle.url)
- [Espais d’Emmagatzematge (Windows)](https://moodle.url)


## Solució
[Solució](Solució.md)
