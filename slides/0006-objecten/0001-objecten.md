### Het zelf maken van objecten

```java 

@Test
public void hetAanmakenVanRoald() {
	Persoon roald; // maak een doosje -> reference persoon object
	
}
```

* We moeten een object maken van het type Persoon 
* Het type Persoon bestaat nog niet
* In java is echter class synoniem voor bouwtekening
* We kunnen zelf een class maken met de naam Person


---=


### De class Persoon


```java 

public class Persoon{


}
```

* De Persoon class is een leeg omhulsel
* Er is nog niet beschreven wat een object van dit type moet
	1. weten
	1. doen
* We kunnen al wel een (bijna kaal) object instantieeren.


---


```java
@Test
public void hetAanmakenVanRoald() {
	
	Persoon roald;
	// maak een doosje -> mag een reference naar persoon object in
	
	roald = new Persoon();
	// de new operator -> maakt een nieuwe persoon object aan
	
}
```


---

### class als bouwtekening

* Wat moet de class kunnen -> opnemen in bouwtekening

```java

@Test
public void hetAanmakenVanRoaldEnFerwin() {
	Persoon persoon1 = new Persoon();
	
	persoon1.setNaam("Roald");
	
	persoon1.setLeeftijd(52);
	
	String naam=persoon1.getNaam();
	
	int leeftijd=persoon1.getLeeftijd();
	
	System.out.println("Persoon met naam " + naam + " met leeftijd " + leeftijd);
}
```


---


@Test
public void hetAanmakenVanRoaldEnFerwin() {
	Persoon persoon1 = new Persoon();
	
	persoon1.setNaam("Roald");
	
	persoon1.setLeeftijd(52);
	
	String naam=persoon1.getNaam();
	
	int leeftijd=persoon1.getLeeftijd();
	
	System.out.println("Persoon met naam " + naam + " met leeftijd " + leeftijd);
	
	Persoon persoon2 = new Persoon();
	
	persoon2.setNaam("Ferwin");
	
	persoon2.setLeeftijd(52);
	
	String naam2 = persoon2.getNaam();
	
	System.out.println(naam2);
}

//Nabouwen van bovenstaande

@Test
public void watKunnenWeNuMetReferenceVariabelen() {
	//8 primitivetypes -> the value is stored inside the variabel
	byte byteDoosje=1;
	short shortDoosje=32000;
	int intDoosje=2_000_000;
	long longDoosje=1_000_000_000L;
	float floatDoosje=1.0F;
	double doubleDoosje=1.0;
	boolean trueFalseDoosje=true;
	char charDoosje='a';
	
	//The Reference types
	
	Persoon persoon1 = new Persoon();
	
	 
	
	System.out.println("Naam = " + persoon1.getNaam() + " en leeftijd = " + persoon1.getLeeftijd() + " en humor = " + persoon1.getHumor());
	
	
	
}



@Test
public void eenObjectDatAangemaaktIsBevindZichAltijdInWelgedefineerdeToestand() {
	
	Persoon persoon1 = new Persoon();
	
	System.out.println("Leeftijd = " + persoon1.getLeeftijd() + " en humor = " + persoon1.getHumor());
	
	//-> primitive instance variabelen worden op 0 of 0.0 of false geinitialiseerd
	
	System.out.println("De naam = " + persoon1.getNaam());
	
	// -> Een Reference instancevariabele die geen waarde krijgt wordt op null geinitialiseerd -> ik wijs nergens naar
}





@Test
public void watGebeurtErHier() {
	Persoon persoon2= new Persoon();
	persoon2.setLeeftijd(56);
	persoon2.setNaam("Roald");
	
	Persoon diePeter= new Persoon();
	diePeter.setNaam("Peter");
	diePeter.setLeeftijd(49);
	
	Persoon anderePeter= new Persoon();
	anderePeter.setNaam("Peter");
	anderePeter.setLeeftijd(53);
	
	//We zijn hier bij het uitvoeren van de code
	
	System.out.println("De naam = " + persoon2.getNaam() + "Leeftijd = " + persoon2.getLeeftijd() + " en humor = " + persoon2.getHumor());
	System.out.println("De naam = " + diePeter.getNaam() + "Leeftijd = " + diePeter.getLeeftijd() + " en humor = " + diePeter.getHumor());
	System.out.println("De naam = " + anderePeter.getNaam() + "Leeftijd = " + anderePeter.getLeeftijd() + " en humor = " + anderePeter.getHumor());
	
}

@Test
public void enWatGebeurtErHier() {
	
	Persoon persoon2= new Persoon("Roald",56);
	
	Persoon diePeter= new Persoon("Peter",49);
	
	
	Persoon anderePeter= new Persoon("Peter",53);
	
	//We zijn hier bij het uitvoeren van de code
	
	System.out.println("De naam = " + persoon2.getNaam() + "Leeftijd = " + persoon2.getLeeftijd() + " en humor = " + persoon2.getHumor());
	System.out.println("De naam = " + diePeter.getNaam() + "Leeftijd = " + diePeter.getLeeftijd() + " en humor = " + diePeter.getHumor());
	System.out.println("De naam = " + anderePeter.getNaam() + "Leeftijd = " + anderePeter.getLeeftijd() + " en humor = " + anderePeter.getHumor());
	
}



@Test
public void deToestandVeranderenInEenObject() {
	Persoon persoon = new Persoon("Roald",-56);
	
	//persoon.humor=true;
	
	System.out.println("De naam = " + persoon.getNaam() + "Leeftijd = " + persoon.getLeeftijd() + " en humor = " + persoon.getHumor());
	
}












