### Giving blocks a name

* Start with last example: calculation the table of 7


```java

@Test
public void uitwerkingPrintenVanDeTafelVan7(){

	int finishedLoops = 0;
	int multiplyBy = 1;

	while (finishedLoops < 10) {
		System.out.println(multiplyBy + " * 7 = " +multiplyBy * 7);
		multiplyBy = multiplyBy + 1;
		finishedLoops = finishedLoops + 1;
	}
}
```


---


#### The table of 7

* What part of the code is really about the table of 7?


```java

@Test
public void uitwerkingPrintenVanDeTafelVan7(){

	{
	int finishedLoops = 0;
	int multiplyBy = 1;

		while (finishedLoops < 10) {
			System.out.println(multiplyBy + " * 7 = " +multiplyBy * 7);
			multiplyBy = multiplyBy + 1;
			finishedLoops = finishedLoops + 1;
		}
	}

}
```



---


### Gives block a descriptive name

```java

@Test
public void uitwerkingPrintenVanDeTafelVan7() {

	tafelVan7() // <- When block receives a name () are necessary
	{
		int finishedLoops = 0;
		int multiplyBy = 1;

		while (finishedLoops < 10) {
			System.out.println(multiplyBy + " * 7 = " +multiplyBy * 7);
			multiplyBy = multiplyBy + 1;
			finishedLoops = finishedLoops + 1;
		}
	}
}
```


---


#### Rules about naming a block of code

* It is not allowed to give a block of code a name inside another block
* A block of code can supply a return value, it can give back a value
* In Java you must specify the type a block can return
* If the block does not return anything you should use void as a returntype.


---


### The code

* tafelVan7() is called a method

```java

void tafelVan7(){
	int finishedLoops = 0;
	int multiplyBy = 1;

	while (finishedLoops < 10) {
		System.out.println(multiplyBy + " * 7 = " + multiplyBy * 7);

		multiplyBy = multiplyBy + 1;
		finishedLoops = finishedLoops + 1;
	}
}
```

---


### Calling a method

* In the code the codeblock is executed twice

```java

@Test
public void generalisatie(){
	
	// block code geven we een naam
	tafelVan7();
	tafelVan7();

}
```



---


### Een methode generieker maken

```java
void tafelVan7Opgeschoond(){
	int finishedLoops = 0;
	int multiplyBy = 1;

	while (finishedLoops < 10) {
		p(multiplyBy + " * 7 = " + multiplyBy * 7);

		multiplyBy = multiplyBy + 1;
		finishedLoops = finishedLoops + 1;
	}
}
```


---

### Introductie lokale variabele

```java
void tafelVan() {
	int grondTal = 7 ; // of maak 8
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

##### Zou het niet handig zijn om bij het aanroepen te kunnen meegeven wat de tafel moet doen?

```java
@Test
public void voerDeTafelVan7EnVan8Uit(){
	tafelVan(7);
	tafelVan(8);
}
```


---

### Introductie parameter

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


### Aanroepen van het code blok met parameter

```java
@Test
public void voerDeTafelVan7EnVan8Uit(){
	tafelVan(7);
	tafelVan(8);
}
```


---


### System.out.println veel typen!

```java

@Test
public void getRidOfSystemoutprintln(){
	// Hier hebben we wel een block code uitgehaald
	// Hier roepen we de methode aan

	p();

	p("nog een andere string");

	// methods with the same name but with different
	// number of parameters or type of parameter are allowed in Java
	// This is called method overloading
}
```

---


### Methods with the same name

```java 
// declareren we een methode
void p(){
	System.out.println("**************************");
}
//String input wordt parameter genoemd
void p(String input){
	System.out.println(input);
}
```


---


### Methode overloading


* methodes in java mogen de zelfde naam hebben
* methodes moeten dan wel verschillen in
  * aantal parameters
  * of type van parameters


