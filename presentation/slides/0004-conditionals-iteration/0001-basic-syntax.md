### Basic syntax explored

```java

	@Test 
	void hoeZietDeJavaSyntaxErEigenlijkUit() {
		// Met { .... } definieren we een code blok
		System.out.println("Start van code blok");
			
		{   //blocken kun je ook nesten
			System.out.println("Start van inner code blok");
			System.out.println("Einde van inner code blok");
		}
		System.out.println("Einde van code blok");
	}
```


---


### Scope van variabelen

```java
void hoeZitHetMetVariabelenEnCodeBlocken() {
	System.out.println("Start van code blok");
	boolean outerBlokBoolean=true;
	System.out.println("Outer block boolean = " + outerBlokBoolean);	
	{
		System.out.println("Start van inner code blok");
		boolean innerBlokBoolean=true;
		System.out.println("Inner block boolean = " + innerBlokBoolean);
		System.out.println("Outer block boolean = " + outerBlokBoolean);
		System.out.println("Einde van inner code blok");
	}
	//System.out.println("Inner block boolean = " + innerBlokBoolean);
	System.out.println("Outer block boolean = " + outerBlokBoolean);	
	System.out.println("Einde van code blok");
}
```


---

### Scope van een variabele

		
* variable is zichtbaar binnen het block waarin het gedeclareerd wordt inclusief geneste blocken
* variabelen gedeclareerd in een genest block is buiten dat blok niet zichtbaar
* het block (inclusief geneste blocken) waarbinnen de variabele gebruikt kan worden wordt ook wel de scope van de variabele genoemd



---


### Een blok wel of niet uitvoeren

```java	
void hoeKunnenWeEenBlockConditioneelUitvoeren() {
	System.out.println("Start van code blok");
	
	boolean innerBlockUitvoeren=false;
	
	//Het geneste block willen we conditioneel uitvoeren
	//Syntax:if(conditie){ statements} -> 
	//als conditie true dan statements uitvoeren
	if(innerBlockUitvoeren) 
	{
		System.out.println("Start van inner code blok");
		System.out.println("Einde van inner code blok");
	}
	System.out.println("Einde van code blok");
}
```


---


### Of het een of het andere

```java
void hoeKunnenHetEneBlockOfHetAndereBlockConditioneelUitvoeren() {
		System.out.println("Start van code blok");
		boolean uitvoerenBlok1=true;
		if(uitvoerenBlok1)
		{
			System.out.println("Start van inner code blok1");
			System.out.println("Einde van inner code blok1");
		}
		else
		{
			System.out.println("Start van inner code blok2");
			System.out.println("Einde van inner code blok2");
		}
		System.out.println("Einde van code blok");	
	}
```


---


### Veel gebruikte syntaxconventie


```java
void gebruikVanSyntaxConventies() {
		System.out.println("Start van code blok");
		
		boolean uitvoerenBlok1=true;
		if(uitvoerenBlok1){
			System.out.println("Start van inner code blok1");
			System.out.println("Einde van inner code blok1");
		}else{
			System.out.println("Start van inner code blok2");
			System.out.println("Einde van inner code blok2");
		}
		System.out.println("Einde van code blok");
	}
```


---


### Herhalen van een blok

```java
void hoeKunnenWeHetGenesteBlokEenAantalKerenHerhalen() {
		// Met { .... } definieren we een blok
		System.out.println("Start van code blok");
		//Voorbeeld van oneindige loop	
		while(true)
		{
			//blocken kun je ook nesten
			System.out.println("Start van inner code blok");
			
			System.out.println("Einde van inner code blok");
		}
		//System.out.println("Einde van code blok");
	}
```


---


### Vast aantal keer herhalen van blok

```java
@Test
public void hoeKunnenWeHetGenesteBlok10KeerHerhalen() {
	int aantalHerhalingen=10;
	int loopNr=1;
	boolean conditie=true;
	while(conditie)
	{	
		System.out.println("loopNr = " + loopNr
		 + " aantalHerhalingen = " + aantalHerhalingen);
		conditie=loopNr <= aantalHerhalingen;
		loopNr=loopNr+1;
	}
}
```


---


### Restructure code in while statement

```java
int aantalHerhalingen=10;
int loopNr=1;
boolean conditie=true;
while(conditie)
{
	// Doe useful work
	conditie=loopNr <= aantalHerhalingen;
	loopNr=loopNr+1;
}// restructure into 
while(conditie=loopNr <= aantalHerhalingen)
{
	// Doe useful work
	loopNr=loopNr+1;
}
```


---


### Translate while into for loop

```java
int aantalHerhalingen=10;
int loopNr=1;
while(loopNr <= aantalHerhalingen)
{
	// Doe useful work
	loopNr=loopNr+1;
}
//translate into:
for(int loopNr=1;loopNr <= aantalHerhalingen;loopNr=loopNr+1;){
	// Doe useful work
}
```

---

### Opdracht

* Druk de tafel van 7 af in een nieuwe test
	* Gebruik System.out.println
	* Druk voor 1 t\m 10 af: 1 * 7 = 7 etc.
	* Gebruik variabelen 
	* Gebruik een while loop
* Maak in een nieuwe test een 2de oplossing van de tafel van 7 waarbij je een for loop gebruikt
* Maak in een nieuwe test de tafel van 8 die je wederom print naar de Console
