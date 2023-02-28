# UML

![image](https://user-images.githubusercontent.com/110727546/221840090-78a1dc01-4890-4d2f-a8b4-ee90d587489d.png)

## Definició

UML (Unified Modeling Language) és una manera d'estandaritzar la programació orientada a objectes.

Imagina que vols dibuixar els objectes d'un programa que estas dissenyant i el seu comportament i relació entre ells, aquest "plànol" que fas potser només l'entens tú.

Aquí intervé UML, definint "com" han de dibuixar-se els objectes, les relacions entre sí i el seu comportament que farà que funcioni el programa a implementar.

UML es basa en diagrames que estableixen les especificacions i documentació de qualsevol sistema. Aquests diagrames estan classificats ens diagrames estàtics i diagrames dinàmics, composant un total de 14 diagrames.

## Diagrames

Els diagrames es separen en dos grups: estàtics i dinàmics.

![image](https://user-images.githubusercontent.com/110727546/221979766-0cc20530-22c3-4ed0-be3c-79e3ee592668.png)

### Diagrames estàtics

Ofereixen una visió estructural del model del sistema a desenvolupar.

![image](https://user-images.githubusercontent.com/110727546/221980647-f50f46b7-5eaf-40df-84ec-b34489a7b2cd.png)

- **Diagrama de paquets**, que representa essencialment les relacions de diferents menes entre els continguts de diferents paquets d’un model.
- **Diagrama de classes**, que probablement molts consideren el diagrama principal, atès que descriu classificadors de tota mena i diferents tipus de relacions entre ells abans de fer-los servir en altres diagrames.
- **Diagrama d’objectes**, que representa instàncies de classificadors definits en un diagrama de classes previ i relacions entre elles.
- **Diagrama d’estructures compostes**, que descriu casos en què, o bé les instàncies d’un classificador tenen com a parts instàncies d’altres, o bé en el comportament executant d’un classificador participen instàncies d’altres.
- **Diagrama de components**, que és un diagrama de classes i alhora d’estructures compostes simplificat i més adient per a determinades tecnologies de programació.
- **Diagrama de desplegament**, que descriu la configuració en temps d’execució d’un programari especificat, normalment, per un diagrama de components.
- **Diagrama de perfil**, permet adaptar o personalitzar el model amb construccions que són específiques d’un domini en particular, d’una determinada plataforma, o d’un mètode de desenvolupament de programari…

D'aquests diagrames aprofundirem en el **diagrama de classes**.

### Diagrames dinàmics

Ofereixen una visió del comportament dinàmic del sistema, és a dir, què ha de passar al sistema.

![image](https://user-images.githubusercontent.com/110727546/221981395-7ec69360-df7f-41db-a8a7-a85d7c8218b0.png)

- **Diagrama de casos d’ús**, que considera els comportaments d’un sistema principalment des del punt de vista de les interaccions que té amb el món exterior.
- **Diagrama d’estats**, en el qual es descriuen les diferents situacions -estats- des del punt de vista dels seus comportaments, de les instàncies d’un classificador, alhora que les causes, condicions i conseqüències dels canvis d’una situació a una altra.
- **Diagrama d’activitats**, en què es descriu un comportament complex en forma de seqüències condicionals d’activitats components.
- **Diagrama d’interacció**, que descriu comportaments emergents i té les variants següents:
  - **Diagrama de seqüències**, que fa èmfasi en la seqüència temporal de les participacions de les diferents instàncies.
  - **Diagrama de comunicacions**, que es basa directament en una estructura composta.
  -** Diagrama de visió general de la interacció**, que dóna una visió resumida del comportament emergent.
  - **Diagrama temporal**, que es basa en un diagrama d’estats previ o més d’un i alhora posa èmfasi en els canvis d’estat al llarg del temps.
