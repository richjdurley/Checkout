# TDD Kata

## Acme MultiBuy Checkout Kata
based on Kata @ http://codekata.com/kata/kata09-back-to-the-checkout/

- Think of a self service `CHECKOUT` that allows a customer to `SCAN` each `ITEM` to their `BASKET` in turn and `PRINT` a `RECEIPT` for the items they have purchased.  
- The receipt shows each `ITEM` and it's `UNIT PRICE`.  
- Additionally Acme has a `SPECIAL PRICING RULE` that allows customers to receive a `DISCOUNT` when purchasing multiples of the same item (e.g. 3 for 130). 
- These `MultiBuy Savings` are shown in summary at the bottom of the receipt. 
- Finally the `TOTAL` of the `BASKET` minus multibuy savings is printed at the end of the receipt.

An example stub for the checkout is provided.

```java
public interface Checkout {
  void scan(String item);
  void printReceipt();
}
```
### Required Behaviour

- Implement a simple checkout process that allows items to be scanned (one by one) to a customers checkout basket and a receipt printed as per the below example.  

- For the kata the receipt can be printed using ``print`` methods of ``java.io.PrintWriter`` and passed as a dependency to the receipt printer.

```   
  Item               Price
  ------------------------
    A                   50
    A                   50
    C                   20
    A                   50
    D                   15
    
  MultiBuy Savings
  ------------------------
    A   3-for-130      -20
    
  TOTAL                165
  ------------------------         
```

- Implement item unit pricing and multi-buy special pricing rules using the pricing table below.

```
  Item   Unit      Special
         Price     Price
  --------------------------
    A     50       3 for 130
    B     30       2 for 45
    C     20
    D     15
```

- Assume each item is scanned through the `checkout` in turn
- Assume the customer payment process is out of scope
- Assume that all items scanned will have a price

### Developer rules
- Must use a strict TDD process
- Must not use abbreviations
- Must apply SOLID principles
- Must implement an Event sourcing pattern
- Must use dependency inversion
- Should use lamda programming style where appropriate

### Guidence
- Begin with writing
  1) Checkout scan functionality 
  2) Then adding basic receipt printing 
  3) finally adding the special pricing rules and multibuy receipt printing
- What are the major entities / what design do you have in mind
- In which entity could a simple Event sourcing pattern be implemented ?
- What acceptance tests do you need to write ?
- Which behaviours do you need to test ?
- Do you need to use Mocking ?
