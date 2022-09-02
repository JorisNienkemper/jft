## De debugger

---

### Inzicht krijgen in code executie

```java
@Test
public void voerDeTafelVan7EnVan8Uit(){
	tafelVan(7);
}
```

---

### We willen inzicht krijgen in de code

```java
void tafelVan(int grondTal) {
	int finishedLoops = 0;
	int multiplyBy = 1;

	while (finishedLoops < 10) {
		p(multiplyBy + " * " + grondTal + " = " + multiplyBy * grondTal);
		multiplyBy = multiplyBy + 1;
		finishedLoops = finishedLoops + 1;
	}
}
```

---

### Zet een breakpoint

* De rode stip in kantlijn

![debugging next step](../../img/debug01.png)

---

### Hoover over de start test knop

* De debug optie wordt dan getoond

![debugging next step](../../img/debug02.png)

---

### De code wordt uitgevoerd

* De debugger pauzeert met executie code wanneer het een breakpoint tegenkomt
* Het statement dat blauw gekleurd is, is nog niet uitgevoerd

![debugging next step](../../img/debug03.png)

---

### De debugger opties

* Met **Step Into** kunnen we nu elk statement in de tafelVan methode uitvoeren

![debugging next step](../../img/debug04.png)

---

#### Statement voor statement uitvoeren

![debugging next step](../../img/debug05.png)

---

### Inzicht in waardes van variabelen

* De debugger toont ook een view met de actuele waarden van variabelen

![debugging next step](../../img/debug06.png)

---

#### Hoe vaak zijn we door de while loop gelopen?

![debugging next step](../../img/debug07.png)

* Waarom heeft finishedLoops de waarde 0 en 1?

---

### De actuele waarde van variabelen

![debugging next step](../../img/debug08.png)

---

#### Hoe vaak zijn we door de while loop gelopen?

![debugging next step](../../img/debug09.png)


---



