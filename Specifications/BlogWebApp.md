# BlogWebApp

## Specification
* Simple blogging webapp.
* You do not need to worry about the user interface.
* Use TDD techniques such as mocking, faking and stubs to fake database entries.
* User can create, edit and delete his own entries (posts).
* User cannot edit or delete other user's entries (posts).
* User can add tag to blog post entry.
* Any user can comment on other user's entries (posts).
* Any user can search for tags, recent entries, and blogs with certain tags.

## Scenarios:
Try to develop your own blog software featuring:
**Scenario:** user A posts a new entry<br>
  Given user A posts a new entry<br>
  Then user A can see user A entry<br>
  And user B can see user A entry<br>

**Scenario:** user A deletes a new entry<br>
  Given user A posts a new entry<br>
  And user A deletes the entry<br>
  Then entry cannot be found in the database<br>
  
**Scenario:** user B deletes a new entry<br>
  Given user A posts a new entry<br>
  And user B edits the entry<br>
  Then warning is issued and deletion is halted<br>
  
**Scenario:** user A edits a new entry<br>
  Given user A posts a new entry<br>
  And user A edits the entry<br>
  Then user A can see user A entry<br>
  And user B can see user A entry<br>
  
**Scenario:** user B edits a new entry<br>
  Given user A posts a new entry<br>
  And user B edits the entry<br>
  Then warning is issued and deletion is halted<br>
  
**Scenario:** user B search for user A 10 most recent entries<br>
  Given user A posts a new entry<br>
  And user A posts a new entry<br>
  And user A posts a new entry<br>
  And user A posts a new entry<br>
  And user A posts a new entry<br>
  And user B searches for the last 5 entries<br>
  Then user B can see user A last 5 entries titles<br>
  
**Scenario:** user A tags a new entry<br>
  Given user A posts a new entry<br>
  And user A tags the entry<br>
  Then user A can see the tag on the entry<br>
  And user B can see the tag on the entry<br>
  
**Scenario:** user B attempts to tag user A entry<br>
  Given user A posts a new entry<br>
  And user B tags the entry<br>
  Then warning is issued and tag is not added<br>
  
**Scenario:** user A searches for all tags<br>
  Given user A posts a new entry<br>
  And adds a new tag to the entry<br>
  And user A posts a new entry<br>
  And adds a new tag to the entry<br>
  And user A posts a new entry<br>
  And adds a new tag to the entry<br>
  And user A posts a new entry<br>
  And adds a new tag to the entry<br>
  And user A posts a new entry<br>
  And adds a new tag to the entry<br>
  Then user A can see all the tags in his blog<br>
  
**Scenario:** user B searches for all tags<br>
  Given user A posts a new entry<br>
  And adds a new tag to the entry<br>
  And user A posts a new entry<br>
  And adds a new tag to the entry<br>
  And user A posts a new entry<br>
  And adds a new tag to the entry<br>
  And user A posts a new entry<br>
  And adds a new tag to the entry<br>
  And user A posts a new entry<br>
  And adds a new tag to the entry<br>
  Then user B can see all the tags in his blog<br>

  
* Post new entry
* Delete existing entry
* Update existing entry
* Show 10 most recent entries
* Tag an entry
* Show all tags
* Show blog entry with a certain tag
* etc...
