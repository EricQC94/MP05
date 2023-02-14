# Refacció

La refacció és fer adaptacions en el codi font sense provocar canvis en les operacions del programari.

Amb la refacció s'intenta:
- Prevenció de l’aparició de problemes habituals a partir dels canvis provocats pels manteniments de les aplicacions.
- Ajuda a augmentar la simplicitat del disseny.
- Major enteniment de les estructures de programació.
- Detecció més senzilla d’errors.
- Permet agilitzar la programació.

**Refactorització a IntelliJ:**

![image](https://user-images.githubusercontent.com/110727546/218719920-c4d2bfb8-e38b-4255-bbc5-b6eaa0b2adac.png)

## Patrons de refacció:

Els patrons ofereixen una solució a un problema estàndard que pugui aparèixer mentre estem programant.

Els més habituals són:

- Reanomenar.
- Moure.
- Extreure una variable local.
- Extreure una constant.
- Convertir una variable local en un camp.
- Extreure una interfície.
- Extreure un mètode.

### Reanomenar:

Aquest patró canvia el nom de variables, classes, mètodes, paquets... Tenint en compte les seves referències.

Exemple:

Per canviar el nom del mètode altaAliment a tot el programa pressionem botó dret del ratolí->Refactor->Rename.

![image](https://user-images.githubusercontent.com/110727546/218720860-b41a5d4c-bbe1-4721-9c9a-08b52252b10f.png)

Resultat:

![image](https://user-images.githubusercontent.com/110727546/218720972-9f72ef8e-9a13-4267-84e0-96df3705f1ae.png)

En aquest cas al canviar el nom del mètode canviem també el nom a les crides que es fan a la funció a la resta del programa.

### Moure:

Mou un mètode d'una classe a una altra.

Exemple:

![image](https://user-images.githubusercontent.com/110727546/218721983-e4cfbaf5-5055-49a1-9d13-ae65882d27be.png)

![image](https://user-images.githubusercontent.com/110727546/218722088-d91da50e-560c-48f7-bf88-cff7adf7d7c1.png)

Resultat:

![image](https://user-images.githubusercontent.com/110727546/218722162-11f0b26d-d0d8-42d1-8bdf-85d002757abb.png)

### Extreure una variable local:

Útil si tenim un valor que fem servir molt.

Exemple:

![image](https://user-images.githubusercontent.com/110727546/218722787-098ed242-5443-413e-8ecb-b8a35352714b.png)

![image](https://user-images.githubusercontent.com/110727546/218722957-80e98a57-e1bd-4e1f-8358-c93a0123af43.png)

![image](https://user-images.githubusercontent.com/110727546/218723087-95210eac-3fd3-47bf-a440-3e109269a4c6.png)

Resultat:

![image](https://user-images.githubusercontent.com/110727546/218723175-8017122c-19df-4765-9f1d-930efdda8756.png)

### Extreure una constant:

Exactament igual que el cas anterior però per a variables que no varien mai el seu valor (constants).

Exemple:

![image](https://user-images.githubusercontent.com/110727546/218722787-098ed242-5443-413e-8ecb-b8a35352714b.png)

Resultat:
![image](https://user-images.githubusercontent.com/110727546/218723737-3ee97005-f595-4040-bbe1-a28f0a48d7b7.png)

![image](https://user-images.githubusercontent.com/110727546/218723684-68a870e3-e2b2-4677-80d6-50a10f7ecd21.png)

### Convertir una variable local en un camp (atribut de classe):

Una variable local d'un mètode passa a ser un atribut de classe i, per tant, accesible a tota la classe.

Exemple:

![image](https://user-images.githubusercontent.com/110727546/218724405-1a665939-f3d9-4f9f-b082-ee6e8fd1a850.png)

![image](https://user-images.githubusercontent.com/110727546/218724501-af8a7117-40ac-4a55-9671-fa5dfcab90cd.png)

Resultat:

![image](https://user-images.githubusercontent.com/110727546/218724592-7025a706-a314-451b-9d1d-54ff33169c99.png)

![image](https://user-images.githubusercontent.com/110727546/218724654-82a3f021-eda1-4739-95bd-4d9f8f6ecc63.png)

### Extreure una interfície:

Una interfície es una estructura de Java sense implementar el seu codi, només especificant els seus atributs i mètodes. 

Exemple:

![image](https://user-images.githubusercontent.com/110727546/218864720-efb93c8c-f55e-4c0d-a46a-055fbb12805c.png)

![image](https://user-images.githubusercontent.com/110727546/218864791-6ae77708-bdd7-4272-956a-dda8b1936244.png)

![image](https://user-images.githubusercontent.com/110727546/218864876-eede8367-2009-42c1-a604-944e374bb11a.png)

Resultat:

![image](https://user-images.githubusercontent.com/110727546/218864939-cc176388-0576-460e-a6e9-3531a9032389.png)

![image](https://user-images.githubusercontent.com/110727546/218864970-7c571793-4264-4049-a84e-c6d94b3ae7cb.png)

### Extreure un mètode:

Quan utilitzem un bloc de codi més d'una vegada és millor passar-ho a una funció.

Exemple:

![image](https://user-images.githubusercontent.com/110727546/218866683-e2a0fd65-8bc0-43d9-beeb-fb1c576d0819.png)

![image](https://user-images.githubusercontent.com/110727546/218866780-85e1d1b5-d84d-4542-866a-184d0b139e8f.png)

Resultat:

![image](https://user-images.githubusercontent.com/110727546/218866905-2e5e975f-3bb7-4c0a-8f1f-c84fd1a5db51.png)

![image](https://user-images.githubusercontent.com/110727546/218867049-faf38688-1b8a-4542-a50f-33db455ce9ec.png)

