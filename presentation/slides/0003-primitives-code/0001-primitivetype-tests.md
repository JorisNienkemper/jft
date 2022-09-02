#### Hoe zouden jullie het concept variable beschrijven?

	* een doosje/container
	* is er voor een bepaalde tijd
	* doosjes specifiek voor bepaalde inhoud
	* kunt er iets instoppen/uithalen
	* kunt het hergebruiken


---

## Typesystem Java

* 2 hoofdtakken
    * primitivetypes
    * referencetypes

* Kijken eerst naar primitivetypes -> 8 in totaal


---


## Variabelen

* create new maven java project

```java
package org.example

import static org.junit.Assert.*;

import org.junit.Test;

public class ExploreJavaPrimitives {

	@Test
	public void declaarIntVariabeleEnAssignDeWaarde10() {
		//Schrijf hier code

	}
}
```

---


### Waarde past niet niet in doosje

```java
@Test
public void doosjesKunnenNietOnbeperktGroteGetallenBevatten() {
	// 4 bytes groot en 32 posities
	int doosje;
	
	// 2 forward slashes is een line comment
	// er is een max aan het getal dat we kunnen opslaan.
	doosje=1000000000; // Dit lukt nog net
	doosje=Long.MAX_VALUE; //Lukt niet

}
```

---

### Primitive types:

* doosjes in java moeten getypeerd zijn
	* d.w.z. java wil van te voren weten wat je er in stopt

* we zullen allereerst stilstaan bij de primitive types
* later gaan we naar de reference types kijken


---



### Kleinste type voor gehele getallen 

* byte -> 8 bits

```java
@Test
public void kleinsteMaatVoorGeheleGetallen() {
	byte doosjeVoor1Byte;
	doosjeVoor1Byte=1;
	System.out.println(doosjeVoor1Byte);
}
	
```

---


### Byte MAX_VALUE


```java
@Test
public void omslagPuntVanMaximaleGrootteNaarMinimaleGrootte()  {
	byte doosjeVoor1Byte=127;
	System.out.println("Maximale byte waarde = " + doosjeVoor1Byte);
}
```

---

## short 2* grotere capaciteit dan byte

```java
@Test
public void shortIs2KeerZoGrootAlsByte() {
	short shortDoosje=128;
	
	//Opmerkelijk genoeg gaat dit wel goed!
	shortDoosje += 1;
	
	System.out.println(shortDoosje);
}
```

---

##	 long (8 bytes groot)

```java

@Test
public void longTypeIs8BytesLang()  {
	long longDoosje1=9_223_372_036_854_775_807L;
	//long longDoosje2=1l; kleine l niet gebruiken
	
	long maxLongDoosje=Long.MAX_VALUE;
	System.out.println(maxLongDoosje);
}
```
* long's kunnen groot worden, merk de _ (underscore) op als 1000-tal scheider

---

### Variabelen hebben een type en een grootte

* byte/ short/ int/ long
* Je kunt dus een waarde(a.k.a. een literal (2 of 3 of 100 etc.)) in een doosje stoppen
* Die waarde past of past niet
* In het laatste geval klaagt Java!

---

### Waarom heb je variabelen nodig

* Berekeningen

```java
//Verzin met de groep een berekening waarbij je gehele getallen gebruikt
```

---

### double type -> "approximate numerics"

* floatingpoint rekenen

```java

@Test
public void doublesHebben8BytesOmGebrokenGetallenteBeschrijven() {
	double doubleDoosje1=0.2-0.1;
	double doubleDoosje2=0.3-0.2;
	System.out.println(doubleDoosje1-doubleDoosje2);
}
```

* Output in console: 2.7755575615628914E-17


---


### Het float type

```java

@Test
public void byDefaultWordenGebrokenGetallenGezienAlsDouble(){
	float floatDoosje=(float)1.0;
	System.out.println(floatDoosje);
}
	
```
* 1.0 zonder (float) wordt gezien als double -> 8 bytes -> past niet

---

### Waar gebruiken we doubles en floats voor?

* Berekeningen
* Bedenk allemaal een voorbeeld van een berekening waar je deze types gebruikt

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
