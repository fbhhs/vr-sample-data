vr-sample-data
==============

Sample data about the Voting Rights Act
----------------------------------------

originally created 6/14 by Rachel Shorey for Code for Progress. Note that this data is intended for learning SQL, not for learning about or evaluating the content within. The data was (not very carefully) copied from wikipedia and was not checked.

Create table statements included for demonstration purposes. Tested in MySQL, but ymmv elsewhere.

data files:
states (51, incl district of columbia, note that race percents may or may not add to 100):


|field                      | description                     |
|---------------------------|---------------------------------|
| id                        | pkey                            |
| name                      | state name                      |
| population                | state's population              |
| pct_non_hisp_white     | pct white (non-hispanic)        |
| pct_hisp                 | pct hispanic                    |
| pct_black                | pct black                       |
| pct_na                   | pct native american/alaskan     |
| pct_asian                | pct asian                       |
| pct_hpi                  | pct hawaiian pacific islander   |
| pct_mixed                | pct mixed race                  |
| region                    | north, south, midwest, west*    |



*as defined by wikipedia, IT IS NOT MY FAULT THAT THEY THINK DC IS IN THE SOUTH

cities (largest 50 cities in the US as defined by wikipedia):
city
2013pop
area_sq_miles
state_id (foreign key)

sections (sections of the voting rights act that can apply to various states. note that in some cases a section applies to the whole state, while in others it applies to parts of the state. for the purpose of this exercise, I assumed that the state was covered if any part of it was)
id (pkey)
section
description
status

sections_states (join table between sections and states):
section_id (foreign key)
state_id (foreign key)