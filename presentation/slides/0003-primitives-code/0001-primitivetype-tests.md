### Types

---

#### Hoe zouden jullie het concept variable beschrijven?

	* een doosje
	* is er voor een beperkte tijd
	* doosjes specifiek voor bepaalde inhoud
	* kunt er iets instoppen/uithalen
	* kunt het hergebruiken
	* officieel noemen we een doosje een variabele


---

## Type system Java

* In Java moet je als je een variabele maakt aangeven wat je er in stopt 
* Je zegt in Java: Je geeft het type op van de variabele

* 2 hoofdtakken
    * primitive types
    * reference types

* Kijken eerst naar primitive types -> 8 in totaal


---


## Variabelen

* create new maven java project

```java
package org.example

import static org.junit.Assert.*;

import org.junit.Test;

public class ExploreJavaPrimitives {

	@Test
	void skeletonToRunCode() {
		//Schrijf hier code
	}
}
```

---


### Primitive types:

* doosjes in java moeten getypeerd zijn
	* d.w.z. java wil van te voren weten wat je er in wilt stoppen

* we zullen allereerst stilstaan bij de primitive types
* later gaan we naar de reference types kijken


---



### Kleinste doosje voor gehele getallen 

* byte -> 8 bits

```java
@Test
void declareByteVariable(){
    byte temperature;
    temperature = 1; //8bits 0000 0001
    System.out.println(temperature);
}
```

* Is er ook een grootste waarde?
* Wat is de kleinste waarde?

---


### De grootste byte value (MAX_VALUE)


```java
@Test
void declareByteVariable(){
    byte minimumtemperature;
    minimumtemperature = -128; //laagste waarde
	 //8bits 1000 0000
    System.out.println(minimumtemperature);

    byte maximumtemperature = 127;
	//8bits 0111 1111
    System.out.println(maximumtemperature);
}
```

---

## short 

* 2* grotere capaciteit dan byte

```java
    @Test
    void declareShortVariable(){
        short minimumtemperature; 
		//16 bits 0000 00000 0000 0001
        minimumtemperature = -32_000; 
		//In de buurt van de laagste waarde
        System.out.println(minimumtemperature);

        short maximumtemperature = 32_000;
		//In de buurt van de maximale short value
        System.out.println(maximumtemperature);
        //Homework bereken 2 to the power 15
    }
```

---

## int 

* 2* grotere capaciteit dan short

```java
    @Test
    void declareIntVariable(){
        int minimumtemperature; 
		//32 bits 1000 0000 0000 0000 0000 0000 0000 0000
		minimumtemperature = -2000000000;
		// Al die nullen zijn lastig te lezen
        minimumtemperature = -2_000_000_000;
        //Use underscores in int to indicate thousands
        System.out.println(minimumtemperature);

        int maximumtemperature = 2_000_000_000;
		// In de buurt van MAX_VALUE van int
        System.out.println(maximumtemperature);
        //Homework bereken 2 to the power 31
    }
```

* By default worden getallen zonder extra aanduiding door Java gezien als int's

---

##	 long (8 bytes groot)

```java
    @Test
    void declareLongVariable(){
        long minimumtemperature; //64 bits 
        maximumtemperature = 2_100_100_100_100_000_000L;
        //In de buurt van MAX_VALUE long
		//Hoe spreek je dit getal uit?
        System.out.println(maximumtemperature);
        //Homework bereken 2 to the power 63
    }

---

### Variabelen hebben een type en een grootte

* byte/ short/ int/ long
* Je kunt dus een waarde(a.k.a. een literal (2 of 3 of 100 etc.)) in een doosje stoppen
* Die waarde past of past niet
* In het laatste geval klaagt Java!

---

### Waarom heb je variabelen nodig

* Berekeningen
	* Verzin met de groep een berekening waarbij je gehele getallen gebruikt
* Voor berekeningen heb je operatoren nodig
	* Welke operatoren ken je?
	* Hoe zou je operatoren beschrijven?
	* Wat wordt er bedoeld met operanden?
* Ken je regels waar operatoren aan moeten voldoen?

```
---
### Berekening demo 1

```java
    @Test
    void berekenTotaalAantalDeelnemers(){
        int dotNetters = 25;
        int javanen = 12;
        int totaalDeelnemers = dotNetters + javanen;

        System.out.println("Aantal deelnemers " + totaalDeelnemers);
    }
```

---
### Berekening demo 2

```java
   @Test
    void berekenDeDistance(){
        int velocity =10;
        int time= 5;
        int distance = velocity * time;
        System.out.println("De afgelegde afstand " + distance);
    }
```

---
### Berekening demo 3

```java
    @Test
    void aantalBenodigdeWielen(){
        int auto = 32;
        int wielen = 4;

        //int aantalWielen = auto * wielen;

        System.out.println("Aantal wielen =" + auto * wielen);
    }
```
---
### Berekening demo 4

```java
    @Test
    void aantalBenodigdeWielenPlusMinimumVoorraad(){
        int wielen = 32;
        int autos = 4;
        int minimumVoorraad = 16;
		// We verdubbelen het aantal autos
		// In de println autos*2
		// Wat verwacht je?
        System.out.println((wielen - minimumVoorraad)/autos*2);

        //System.out.println((wielen - minimumVoorraad)/(autos*2));
    }
```
---

### Bestaat Meneer van Dalen nog?

* Prioriteit van operatoren
* Hoe zit het ook alweer?
---

### Berekening demo 5

* Wat doet de modulo operator?

```java
    @Test
    void operationsWithTheModuloOperator(){
        System.out.println(1 % 2); //1
        System.out.println(2 % 2); //0
        System.out.println(3 % 2); //1
        System.out.println(4 % 2); //0
        System.out.println(5 % 2); //1
        System.out.println(6 % 2); //0
        System.out.println(7 % 2); //1
    }
```
---

### Berekening demo 6

```java
    @Test
    void welkePrioriteitHeeftDeModuloOperator(){

        System.out.println(3 * 11 % 3);
        System.out.println((3 * 11) % 3); //0
        System.out.println(3 * (11 % 3)); //6
        System.out.println(11 % 3 * 3);
        System.out.println((11 % 3) * 3); //0
        System.out.println(11 % (3 * 3)); //6

    }
```

---

### double type -> "approximate numerics"

* floatingpoint rekenen

```java

@Test
void declareDoubleVariables(){
    //Handig om te onthouden dat er bij doubles (ook bij floats) vaak sprake is van een afronding
    double price = 1.9447;
    double aantalLiters = 45.68;
    double multiplier = 1.0E2; //1.0 keer 10 tot de macht 2 (100)

    System.out.println("Verkoopprijs = " + price * aantalLiters* multiplier);
}
```

---


### Het float type

```java
@Test
public void byDefaultWordenGebrokenGetallenGezienAlsDouble(){
	float floatDoosje=1.0F;
	System.out.println(floatDoosje);
}
```

* 1.0 zonder (F) wordt gezien als double -> 8 bytes -> past niet


---

### Het boolean type

```java
@Test
public void booleansExperiment()  {
	boolean isDoosjeLeeg,isDoosjeVol;
	isDoosjeLeeg=false;
	isDoosjeVol=true;
	System.out.println(isDoosjeLeeg);
	System.out.println(isDoosjeVol);
}

```

* Boolean domein  bevat 2 literal values: true en false

---
### Waar gebruiken we boolean variabelen voor?

```java
@Test
public void opslaanVanVergelijkingen()  {
	boolean heeftMinimumLeeftijd;
	int minimumLeeftijd = 18;
	int leeftijdPiet = 20;
	heeftMinimumLeeftijd = leeftijdPiet >= minimumLeeftijd;
	System.out.println(heeftMinimumLeeftijd);
	//Waar gebruiken we booleans voor?
}

```

### Vergelijkingen combineren 1
 
* Soms moet een conditie aan meer vergelijking voldoen
    1. Een persoon moet meerderjarig zijn **EN**
    2. de Nederlandse nationaliteit bezitten

---

#### Vergelijkingen combineren 2

```java
@Test
public void beideVergelijkingenMoetenWaarZijn()  {
	boolean heeftMinimumLeeftijd;
	int minimumLeeftijd = 18;
	int leeftijdPiet = 20;
	heeftMinimumLeeftijd = leeftijdPiet >= minimumLeeftijd;
	int minimumInkomen = 20_000;
    int inkomenPiet = 25000;
    boolean isBovenMinimumInkomen = inkomenPiet > minimumInkomen;
    boolean voldoetAanBeideCriteria =
    heeftMinimumLeeftijd && isBovenMinimumInkomen;
    System.out.println(voldoetAanBeideCriteria);
	
} 

```
---


#### Vergelijkingen combineren 3

```java
@Test
public void eenVanDe2VergelijkingenMoetWaarZijn()  {
	boolean heeftDagKaart = false;
    boolean heeftMaandKaart = false;
    boolean heeftJaarAbonnement = true;
	boolean heeftGeldigeToegangsBewijs =
    heeftDagKaart || heeftMaandKaart || heeftJaarAbonnement;
    System.out.println(heeftGeldigeToegangsBewijs);
	
} 

```
---

### Het char type

```java

@Test
public void spelenMetChars() {
	char charDoosje1='a';
	char charDoosje2='b';
	System.out.println(charDoosje1 + charDoosje2);
	
	System.out.println("dit is een waarde = " + 10);
	
	System.out.println(charDoosje1 + charDoosje2 + "");
	
}
```
* De + operator ziet char als getallen (unsigned)
* De expressie wordt van links -> rechts geëvalueerd
* "" + 'a' -> String



---

### Resumerend

* 8 primitive types
	* gehele getallen met sign
		1. byte 1 byte
		1. short 2 bytes
		1. int 4 bytes
		1. long 8 bytes
	* floating point
		1. float 4 bytes
		1. double 8 bytes
	* character
	   1. char 2 bytes
	* boolean
	   1. boolean
