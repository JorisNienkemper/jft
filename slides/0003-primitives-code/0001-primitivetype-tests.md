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
package joris.jft.dag0102.primitives;

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


### Variable kan te klein zijn voor een waarde

```java
@Test
public void doosjeKunnenNietOnbeperktGroteGetallenBevatten() {
	// 4 bytes groot en 32 posities
	int doosje;
	
	// 2 forward slashes is een line comment
	// er is een max aan het getal dat we kunnen opslaan.
	doosje=1000000000;
	// dit lukt nog net
	doosje=Long.MAX_VALUE;

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
		doosjeVoor1Byte=(byte)(1 + 1);
		System.out.println(doosjeVoor1Byte);
	}
	
```

---


### Byte MAX_VALU


```java
	@Test
	public void omslagPuntVanMaximaleGrootteNaarMinimaleGrootte()  {
		byte doosjeVoor1Byte=127;
		System.out.println("Maximale byte waarde = " + doosjeVoor1Byte);
		// + operator ziet 2 bytes-> telt tie netjes maar geeft een int terug
		// int is 4 bytes past niet in een byte -> resultaat moet gecast worden
		doosjeVoor1Byte=(byte)(doosjeVoor1Byte + 1);
		System.out.println(doosjeVoor1Byte);
	}
```
* Speciaal gedrag wanneer by de Byte.MAX_VALUE er 1 wordt opgeteld

---

## short 2* grotere capaciteit dan byte

```java
@Test
public void shortIs2KeerZoGrootAlsByte() {
	short shortDoosje=128;
	shortDoosje=(short) (shortDoosje+1);
	
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

### Het boolean type

```java
@Test
public void booleansExperiment()  {
	boolean isDoosjeLeeg;
	isDoosjeLeeg=false;
	//Kijkt uit voor isDoosjeLeeg = isDoosjeLeeg -> dit is geen vergelijking maar een toekenning
	isDoosjeLeeg=(isDoosjeLeeg == isDoosjeLeeg);
	System.out.println(isDoosjeLeeg);
}

```

* Bolean domein  bevat 2 literal values: true en false


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
* De expressie wordt van links -> rechts geevalueerd
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
