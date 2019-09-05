# Coding-Kata
Coding Kata Examples

## A MultiBuy Checkout
based on Kata @ http://codekata.com/kata/kata09-back-to-the-checkout/

Given the example stub.

```java
public interface Checkout {
  void scan(ItemID itemId);
  void printReceipt();
}
```
### Required Behaviour

- Implement a simple checkout process that allows items to be scanned and a receipt printed

- Implement unit pricing and multi-buy special pricing rules using the pricing table below.

```
  Item   Unit      Special
         Price     Price
  --------------------------
    A     50       3 for 130
    B     30       2 for 45
    C     20
    D     15
```

- Assume each item is scanned through the `checkout` process in turn

- Print an example text receipt in a format as follows


```   
  Item              Price
  ------------------------
    A                   50
    A                   50
    C                   20
    A                   50
    D                   15
    
  MultiBuy Savings
  ------------------------
    A   3-for-130      -20
  
  TOTAL                162
  ------------------------         
```

### Developer rules
- Must use a strict TDD process
- Must not use abbreviations
- Must apply SOLID principles
- Should implement using a CQRS / Event sourcing pattern
- Must keep all objects small, highly cohesive and isolated
- Must use dependency inversion
- Should use objects in preference to primitives (e.g. use an Amount object rather than double)
- Should use lamda programming style where appropriate

