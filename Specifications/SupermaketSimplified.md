# Simplified Supermaket Kata

## Specification
We’re going to see how far we can get in implementing a supermarket checkout that calculates the total price of a number of items.  

- In a normal supermarket, things are identified using **Stock Keeping Units**, or **SKU**s.  
- The **SKU** for our 4 products are **A**, **B**, **C**, **D**;
- Our goods are priced individually.  
- In addition, some items are multipriced: buy n of them, and they’ll cost you y pounds.  
  - Item **A** might cost 50 pounds individually, but if you buy three **A**s and they’ll total to 130. 
- The price and offer table:  


|Item | Price | Offer      |
|-----|-------|------------|
|A    | 50    | 3 for 130  |
|B    | 30    | 2 for 45   |
|C    | 20    |            |
|D    | 15    |            | 


- Our checkout accepts items in any order.
  - If we scan a **B**, an **A**, and another **B**, the offer for the two **B**’s should be recognized and client charged 95, not 110.

## Tips:
- The interface to your checkout can be anything you like but we’d suggest passing in a string of SKUs to begin with. 

## Unit Test Examples:
Here are the first few tests to help you get started. Will add tests in other languages as I come across them.

1. Ruby:
```ruby
def price(goods)
   co = CheckOut.new(RULES)
   goods.split(//).each { |item| co.scan(item) }
   co.total
end

def test_totals
  assert_equal(  0, price(""))
  assert_equal( 50, price("A"))
  assert_equal( 80, price("AB"))
  assert_equal(115, price("CDBA"))
  assert_equal(100, price("AA"))
  assert_equal(130, price("AAA"))
  assert_equal(175, price("AAABB"))
end
```


_Credits: adapted from Dave Thomas [Kata Nine](http://codekata.pragprog.com/2007/01/kata_nine_back_.html)_
