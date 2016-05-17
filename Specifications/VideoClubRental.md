# VideoClub Rental

This is a big one. It feels fairly simple but it can grow very quickly.
Based it of an exercise presented by Jason Gorman on his fabulous TDD workshops and built upon it to add some more content.

## Specifications
* Users have their name and email stored.
* Users can specify a wishlist. Users should be notified when their wished title becomes available.
* Wishlist is non-case sensitive.
* Users get charged per rental title £2.5.
* Rentals have a return by date of 15 days, starting on the rental day.
* Rentals returned on time award the user 2 priority points.
* Users get discount with multiple rentals, up to 3 simultaneous rentals £2.5 -> £2.25 -> £1.75.
* Users can donate videos to the library.
* Users get priority points when donating videos (10 points per title).
* Library records must include Title, Director, Release year, number of copies.
* Administrator-level users can create or delete new users
* Administrator-level users can create a new newsletter

## Use-case Scenarios

**Scenario:** User registring to videoclub as an adult<br>
  Given User A registers with name: "Sam", age: 18, email: "sam@aol.com"<br>
  When library registers an entry for User A<br>
  Then library sends User A a welcome email<br>

**Scenario:** User cannot register to videoclub as a minor<br>
  Given User A registers with name: "Sam", age: 17, email: "sam@aol.com"<br>
  When library registers an entry for User A<br>
  Then library does not send a welcome email<br>

**Scenario:** User donates a copy of a non-existing title to the library<br>
  Given "Sam" and "Pawel" are members of the VideoClub<br>
  And "Sam" donates a new title with title: "Star Wars VII", director: "JJ Abrahams" and age: "2015"<br>
  And "Pawel" has a wishlist with title: "Star Wars VII" on it<br>
  Then the library creates a new entry for the title with count 1<br>
  And "Sam" receives 10 loyalty points<br>
  And "Pawel" receives a notification that title: "Star Wars VII" is available<br>

**Scenario:** User donates a copy of an existing title to the library<br>
  Given "Sam" and "Pawel" are members of the VideoClub<br>
  And "Sam" donates a new title with title: "Star Wars VII", director: "JJ Abrahams" and age: "2015"<br>
  And "Pawel" has a wishlist with title: "Star Wars VII" on it<br>
  Then the library increases the count for title: "Star Wars VII" by 1<br>
  And "Sam" receives 10 loyalty points<br>
  And "Pawel" receives a notification that title: "Star Wars VII" is available<br>

**Scenario:** user A performs a simple rental<br>
  Given user A is a member of the videoclub<br>
  And title is available for rental<br>
  Then user A can borrow the available copy<br>
  And user A gets charged £2.50<br>
  And library registers the copy as unavailable<br>

**Scenario:** Returning a rental copy<br>
  Given user A performs a simple rental<br>
  And user A returns title<br>
  And user B is number 1 on the waiting list<br>
  Then library registers copy as available<br>
  And sends a thank you email to user A<br>
  And sends a title available email to user B<br> 
  
**Scenario:** Returning the wrong rental copy<br>
  Given user A performs a simple rental<br>
  And user A returns title<br>
  Then library sends an email to user with a warning<br>
  
**Scenario:** Failed to return a rental copy<br>
  Given user A performs a simple rental<br>
  And 16 days later copy is still not returned<br>
  Then library sends an email to the user A<br>
  And prevents user from rental further copies<br>
  And user A looses 2 priority points<br>

**Scenario:** Reserving a rental copy<br>
  Given user A is a video library member<br>
  And user A has more than 5 priority points<br>
  And user A adds title to user A wishlist<br>
  And user B is number 1 in the waiting list<br>
  And user A is number 2 in the waiting list<br>
  And user A requests to have priority access<br>
  And title becomes available for rental<br>
  Then user A gets a notification for availability<br>
  And user B does not get a notification for availability<br>

**Scenario:** Sending newsletter to all members<br>
  Given user A is a administrator user<br>
  And user B is a member user<br>
  And user C is a member user<br>
  And user A sends a newsletter email<br>
  Then user B receives a newsletter email<br>
  And user C receives a newsletter email<br>
