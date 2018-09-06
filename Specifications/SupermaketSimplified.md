# Simplified Supermaket Kata

## Specification
We’re going to see how far we can get in implementing a supermarket checkout that calculates the total price of a number of items.  
In our store, we’ll use individual letters of the alphabet (A, B, C, and so on).  

- In a normal supermarket, things are identified using **Stock Keeping Units**, or **SKU**s.  
- The **SKU** for our 4 products are **A**, **B**, **C**, **D**.
- Our goods are priced individually.  
- In addition, some items are multipriced: buy n of them, and they’ll cost you y pounds.  
  - Item **A** might cost 50 pounds individually, but if you buy three **A**s and they’ll total to 130. 
- Our checkout accepts items in any order.
  - If we scan a **B**, an **A**, and another **B**, the offer for the two **B**’s is applied and client bill is 95, not 110.
- The price and offer table:  


|Item | Price | Offer      |
|-----|-------|------------|
|A    | 50    | 3 for 130  |
|B    | 30    | 2 for 45   |
|C    | 20    |            |
|D    | 15    |            | 


## Tips:
- The interface to your checkout can be anything you like but we’d suggest passing in a string of SKUs to begin with.  
- The challenge lies in the fact the specification doesn’t mention the format of the pricing rules. How can we decouple the system so the checkout doesn’t know about particular items and their pricing strategies?
- Make sure the design is easy enough to allow for item prices and pricing rule changes in the future.
- Because pricing rules and items can change frequently, pricing rules should be passed in as a dependency for each transaction.

### Requirement 1
I want to know the price of an item. These are all the items (there will never be any others)
```
Item  Price  
------------
A     50      
B     30     
C     20
D     15
```

### Requirement 2
Knowing the price was cool. I now want to know the total price of a list of items.

### Requirement 3
I've decided we should be able to offer bulk discounts. Special prices for multiple purchases.
The pricing now works something like this:

```
Item  Price   Offer
--------------------------
A     50       3 for 130
B     30       2 for 45
C     20
D     15
```

### Requirement 4
It'd be cool if we could add new items. Can we have config or something? 
It's okay if the special offers are hard coded.

### Requirement 4b
The special offers can not be hard coded. Why would I have allowed that?

### Requirement 5
I liked the special offer feature can we also have deals like 2 for the price of 1?

### Requirement 6
Can the output have sub totals? And a receipt that shows the discount applied?

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

  def test_incremental
    co = CheckOut.new(RULES)
    assert_equal(  0, co.total)
    co.scan("A");  assert_equal( 50, co.total)
    co.scan("B");  assert_equal( 80, co.total)
    co.scan("A");  assert_equal(130, co.total)
    co.scan("A");  assert_equal(160, co.total)
    co.scan("B");  assert_equal(175, co.total)
  end
```


_Credits: adapted from Dave Thomas [Kata Nine](http://codekata.pragprog.com/2007/01/kata_nine_back_.html)_ and from [7Digital](https://github.com/7digital/kata-checkout)
