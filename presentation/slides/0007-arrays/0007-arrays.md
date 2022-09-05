## Arrays

---

### Werken met veel data

```java
@Test
void slaCijfersOpInGeheugen(){
    int x0,x1,x2,x3,x4,x5,x6,x7,x8,x9;
    x0 = 4;
    x1 = 7;
    x2 = 8;
    x3 = 5;
    x4 = 7;
    x5 = 3;
    x6 = 9;
    x7 = 6;
    x8 = 6;
    x9 = 10;
    System.out.println("x0 = " + x0 + " x1 = " + x1 + " ....etc");
}
```

* Jammer dat we elk stukje data met een unieke naam moeten aanspreken die weinig flexibel is

---

### Arrays to the rescue

```java
@Test
void slaCijfersOpInGeheugen(){
    int[] cijfers = new int[10];
    cijfers[0] = 4;
    cijfers[1] = 7;
    cijfers[2] = 8;
    cijfers[3] = 5;
    cijfers[4] = 7;
    cijfers[5] = 3;
    cijfers[6] = 9;
    cijfers[7] = 6;
    cijfers[8] = 6;
    cijfers[9] = 10;
    System.out.println("x1 = " + cijfers[0] + " x2 = " + cijfers[1] + " ....etc");
}
```

---

### Structuur array

![stuctuur array](../../img/arrays01.png)

---

### Array gebruiken in een for loop

```java
@Test
void printDeAfzonderlijkeCijfers(){
    int[] cijfers = new int[10];
    cijfers[0] = 4;
    cijfers[1] = 7;
    // toekenning andere array-elementen weggelaten


    for (int index = 0; index < cijfers.length; index = index + 1) {
        System.out.println("cijfers[" + index + "] = " + cijfers[index]);
    }
}
```

* We kunnen dus via de index heel makkelijk een array element adresseren.

---

### Een array gevuld met Reference types

```java
@Test
void eenArrayGevuldMetDierenNamen(){
    String [] animalNames= new String[5];
    animalNames[0] = "Kat";
    animalNames[1] = "Leeuw";
    animalNames[2] = "Wolf";
    animalNames[3] = "Blauwevinvis";
    animalNames[4] = "Ekster";
    for (int index = 0; index < animalNames.length; index = index + 1) {
        System.out.println("animalNames[" + index + "] = " + animalNames[index]);
    }
}
```

---

### Opdrachten

* Maak een array die 5 gehele getallen kan bevatten. Elk getal stelt het cijfer voor van een proefwerk waarbij maximaal 100 punten zijn te verdienen en minimaal 10;
    * Maak code die alle cijfers uitprint naar de console
    * Maak code in een nieuwe test die het laagste cijfer uitprint. Kopieer de array uit de vorige test en gebruik de array in deze test en ook in alle volgende testen.
    * Maak code in een nieuwe test die het hoogste cijfer uitprint.
    * Maak code in een nieuwe test die het gemiddelde uitrekent.
    * Pas in de vorige test de data aan. Commentarieer een van de toekenning uit. Bijvoorbeeld
    // cijfers[3] = 7 ;
    Wat gebeurt er met het gemiddelde?
    Waarom? Kijk eventueel met de debugger wat er aan de hand is!
    * Maak code die controleert dat alle cijfers in de range van 10 tot 100 liggen. Wanneer er een getal is dat daarbuiten ligt print dan de index waarvoor dat geldt en de waarde die buiten de range valt.

* Maak van de code in de tests afzonderlijke methodes. Kopieer daartoe de test waar je de methode uit gaat destilleren en pas de naam van de test aan door de er de toevoeging **EnNuMetMethode** aan vast te plakken. Geef de code die je uit de test haalt en in een aparte methode stopt een naam die beschrijft wat de methode doet. Geef alle methodes die je zo maakt een parameter van een geschikt array type. Laat alle methodes ook een waarde retourneren die je vervolgens afdrukt in de test.Geef bij aanroep van de methode de array in de test mee als argument.

* Controleer of de oude test en de nieuwe test waarin je de methode gebruikt nog steeds de zelfde waarde opleveren!

* Maak in een nieuwe test een array van een geschikt type zodat je daar de namen in kunt opslaan van je klasgenoten.
* Maak code die vervolgens de kortste naam uitprint
* Breng de code die de kortste naam vindt onder in een aparte methode
    * De methode verwacht als argument een array van een geschikt type
    * De methode print zelf niet maar geeft de kortste naam terug

    






