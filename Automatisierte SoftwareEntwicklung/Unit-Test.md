



## Sociable vs Solitary 

Imagine you're testing an order class's price method. The price method needs to invoke some functions on the product and customer classes. If you like your unit tests to be solitary, you don't want to use the real product or customer classes here, because a fault in the customer class would cause the order class's tests to fail. Instead you use [TestDoubles](https://martinfowler.com/bliki/TestDouble.html) for the collaborators.


### Self Testing Code 
- can be run quite frequently

## Komponenten Tests
> Automatische Ausführung 

### Gute Unit Tests : 
- isoliert 
- sichern jeweils genau eine Eigenschaft 
- vollständig automatisiert 
- leicht, verständlich, kurz 
- ^

Java Test Frameworks : AssertJ , J Pioneer



