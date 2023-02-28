# UML

## Diagrama de Classes

Una classe és una representació d'un objecte (tangible o intangible) per a ser utilitzat en un programa.

Un diagrama de classes representa les classes que s'utilitzaran dins el sistema i les relacions existents entre elles.

Una classe consta de tres parts principals:
- Nom.
- Atributs.
- Funcions o mètodes.

Representació d'una classe en UML:

![image](https://user-images.githubusercontent.com/110727546/221841590-a3b79ca3-718b-4afa-a12a-d6a7122794f3.png)

**Exemple:** d'exemple farem servir la classe animal

### Nom

El nom de la classe ha de ser representatiu de què és en sí la classe.

![image](https://user-images.githubusercontent.com/110727546/221841686-73c5d8e8-8c25-4184-8695-37f65e3259fe.png)

### Atributs

Els atributs són valors importants de la classe (importants per al nostre programa), també se'ls coneix com propietats o camps.

A la nostra classe animal podem definir alguns atributs com:
- idAnimal (número sencer)
- nom (text)
- edat (número sencer)
- pes (número decimal)

La classe quedaria així:

![image](https://user-images.githubusercontent.com/110727546/221842112-1a15be2b-eee0-412b-ac31-9e2e2029f57b.png)

Però hem de definir també el tipus de dades de cada atribut així que ho especifiquem:

![image](https://user-images.githubusercontent.com/110727546/221849804-d2103b76-93e2-463b-9f73-d2d845271e1c.png)

### Visibilitat

Per últim hem de definir la visibilitat de cada atribut. 

La visibilitat indica qui té accés a l'atribut, hi ha tres valors de visibilitat:
- pública: Pot ser accedit des de qualsevol classe. Símbol (+).
- privada: Només poden ser accedits per la mateixa classe. Símbol (-).
- protegida: Només poden ser accedits per classes del mateix mòdul o subclasses. Símbol (#).
- package: Només pot ser accedit per classes del mateix paquet. Símbol (~).

Així els atributs de la classe, al ser privats quedaran:

![image](https://user-images.githubusercontent.com/110727546/221849729-a50c53b4-801a-4878-a354-9ec244fe07c6.png)

### Operacions

Les operacions o mètodes són funcionalitas de la classe, serveixen per modificar els atributs, realitzar càlculs o altres operacions...

Definirem uns mètodes públics per la nostra classe animal:
- possarNom(nom): Canvia el nom de l'animal pel que li passem.
- pesar(): Retorna el pes de l'animal.
- alimentar(): Donar menjar i aigua a l'animal.

La classe quedarà així:

![image](https://user-images.githubusercontent.com/110727546/221849946-c16e0ebb-2a58-4791-9c7c-c91a0a1d9524.png)

### Objectes

Els objectes són personalitzacions concretes d'una classe, instàncies, espais de memòria amb valors.

Si tenim la classe animal, aquesta defineis a tots els animals possibles, però quan pensem en un animal concret ja és un objecte de la classe animal.

Per exemple, si tenim un gos de 5 anys que es diu "Sultán" i pesa 41kg. Ja no parlem de classe, ara parlem d'un objecte d'una classe o d'una instància de la classe animal.

![image](https://user-images.githubusercontent.com/110727546/221941756-229fbcbe-43ca-49f0-ae5b-c09c7275f333.png)


![image](https://user-images.githubusercontent.com/110727546/221847922-d427d5e8-b422-4ed1-a88e-22a8beb63f15.png)
![image](https://user-images.githubusercontent.com/110727546/221850115-31cf0039-5c6b-4692-a8ea-d406f7884350.png)

## Herència

La classe animal és molt amplia, imagineu que el nostre programa servirà per gestionar diferents parts d'un zoo, hi ha animals que tenen comportaments que no tenen altres, per exemple ens fixem en la secció que cuida les tortugues i la que cuida les ovelles.

Les tortugues hivernen i les ovelles s'han d'esquilar, així que aprofitem que tenen coses comunes a la classe animal i heredem de la classe els seus atributs i mètodes i generem una classe "filla" amb els mètodes i atributs específics.

![image](https://user-images.githubusercontent.com/110727546/221852144-cdc717ea-8680-4cd0-b811-a473aa5c7df3.png)

A l'exemple animal és una **superclasse**, mentre que tortuga i ovella són **subclasses**.

L'herència es representa amb una fletxa que surt de la subclasse i va a la superclasse.

## Relació

Hi ha vegades que dues classes estan relacionades sense ser parents, per exemple: una tortuga pot menjar-se un altre animal, com una medusa.

La relació rep un nom, en aquest cas "menja" i es representa per una línia sense fletxes.

![image](https://user-images.githubusercontent.com/110727546/221935154-2a8b5e23-63e6-4c1b-bb53-c4a7357f18ce.png)

Quan les relacions són entre diferents classes s'anomenen **associacions**.

Les relacions de vegades involucren més d'una instància de cada classe, en l'exemple següent tenim les classes persona i habitació:

![image](https://user-images.githubusercontent.com/110727546/221986963-8035bda1-bb08-4193-9d2e-a58c9feabc23.png)

On podem veure que **UN ÚNIC** objecte de la classe persona  pot fer una reserva d'**UNA O MÉS D'UNA** habitacions.

Per a representar la cardinalitat de les associacions fiquem dos números, un a cada costat de la mateixa. 

![image](https://user-images.githubusercontent.com/110727546/221987681-41e5a952-edcc-48ab-8d17-ed2f43fac446.png)

# Activitat

Escrivim quines associacions poden tenir les següents classes, nom d'associació i cardinalitat:

1. persona, DNI.
2. persona, comics.
3. persona, tren.
4. animal, persona.
5. persona, persona.
6. persona, cotxe.
7. persona, adreça.
8. taxi, client.

## Agregació

Es tracta d'un cas especial d'associació entre dos o més objectes.

Un objecte anomenat base que podrà incloure l'altre tipus d'objectes, com si fos un contingut.

L'objecte base necessita de l'objecte inclòs per existir, però l'objecte inclòs, si desapareix l'objecte base segueix existint.

Exemple: 

Objecte base fruiteria i objectes inclosos diferents tipus de fruita.

![image](https://user-images.githubusercontent.com/110727546/221990480-bbc41b4e-0480-4b82-b06c-ade03f6b4bf5.png)

Les agregacions es representen amb una línia contínua amb un romb buit a l'extrem de l'objecte base.

En aquest exemple si desapareix la fruiteria, les fruites seguiran existint.

# Activitat

Utilitzarem [Lucid](https://lucid.app/) per crear una agregació entre:

1. ovelles, ramat.
2. animals, zoo.
3. curs, estudiants.
4. biblioteca, llibres.
5. atletes, equip.







