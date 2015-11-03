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
**Scenario:** user A posts a new entry
  Given user A posts a new entry
  Then user A can see user A entry
  And user B can see user A entry

**Scenario:** user A deletes a new entry
  Given user A posts a new entry
  And user A deletes the entry
  Then entry cannot be found in the database
  
**Scenario:** user B deletes a new entry
  Given user A posts a new entry
  And user B edits the entry
  Then warning is issued and deletion is halted
  
**Scenario:** user A edits a new entry
  Given user A posts a new entry
  And user A edits the entry
  Then user A can see user A entry
  And user B can see user A entry
  
**Scenario:** user B edits a new entry
  Given user A posts a new entry
  And user B edits the entry
  Then warning is issued and deletion is halted
  
**Scenario:** user B search for user A 10 most recent entries
  Given user A posts a new entry
  And user A posts a new entry
  And user A posts a new entry
  And user A posts a new entry
  And user A posts a new entry
  And user B searches for the last 5 entries
  Then user B can see user A last 5 entries titles
  
**Scenario:** user A tags a new entry
  Given user A posts a new entry
  And user A tags the entry
  Then user A can see the tag on the entry
  And user B can see the tag on the entry
  
**Scenario:** user B attempts to tag user A entry
  Given user A posts a new entry
  And user B tags the entry
  Then warning is issued and tag is not added
  
**Scenario:** user A searches for all tags
  Given user A posts a new entry
  And adds a new tag to the entry
  And user A posts a new entry
  And adds a new tag to the entry
  And user A posts a new entry
  And adds a new tag to the entry
  And user A posts a new entry
  And adds a new tag to the entry
  And user A posts a new entry
  And adds a new tag to the entry
  Then user A can see all the tags in his blog
  
**Scenario:** user B searches for all tags
  Given user A posts a new entry
  And adds a new tag to the entry
  And user A posts a new entry
  And adds a new tag to the entry
  And user A posts a new entry
  And adds a new tag to the entry
  And user A posts a new entry
  And adds a new tag to the entry
  And user A posts a new entry
  And adds a new tag to the entry
  Then user B can see all the tags in his blog

  
* Post new entry
* Delete existing entry
* Update existing entry
* Show 10 most recent entries
* Tag an entry
* Show all tags
* Show blog entry with a certain tag
* etc...
