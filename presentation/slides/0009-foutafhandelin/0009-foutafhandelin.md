## Foutafhandeling

---

### Er gaat iets fout

* Java gooit dan een zogenaamde Exception
* Wat kan er fout gaan?
* Wie kan er iets verzinnen?

---
### Handling basic exceptions

- Using try and catch blocks

---
### Catch or throws

- Code that can throw a certain exception can be enclosed by
    1. A try/catch block, or
---
### 1. try/catch

 - Put the normal code in a try block
 - Handle the exception in an separate catch block
    ````java
    try {
        // statements that can cause SomeException     
        // ...     
    } catch (SomeException e){
        // statements to handle SomeException e 
        // ... 
   }
    ````
---
### try/catch/finally
- optionally, you can add a `finally` to a `try/catch`
   ````java
   try {
       // statements that can cause SomeException     
       // ...     
   } catch (SomeException e){
       // statements to handle SomeException e 
       // ... 
   } finally {
       // these statements are always executed, 
       // e.g. close resources  
   }
   ````

---
### try/finally
- you can add a `finally` to a `try` without a `catch`
  ````java
   try {
       // statements to open a resource     
       // ...     
   } finally {
       // these statements are always executed, 
       // e.g. close resources  
   }
   ````

---

### Guidelines
- Catching
    - Arrange **`catch`** blocks from specific to general
    - Do not let exceptions drop off **`main`** 
- Finally
    - `finally` blocks are always executed
    - useful for closing resources
