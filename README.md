Characters
==========

char_nameDatabase.xml
Example structure of the XML File containing Name data:
~~~
	<Info>
		<Name>Ron Swanson</Name>
		<Gender>0</Gender>
		<Nationality>0</Nationality>
		<Job>Parks &amp; Recreation Officer</Job>
		<History>Hates people\nHates everything</History>
		<Reason>Wants to get as far away from people as he can</Reason>
	</Info>
~~~
These are the fields that can be used for this file.

* Name = Name of the character, to be displayed underneath them and in their Travel Visa.
* Gender = An int of their specific gender. (0 = Male, 1 = Female)
* Nationality = An int of their specific nationality. (0 = American, 1 = Wild West, 2 = Canadian, 3 = European, 4 = Asian, 5 = Russian)
* Job = This specific character's job. If this field is left empty or missing, their job will be randomized from the char_jobDatabase.xml file instead.
* History = This specific character's history. If this field is left empty or missing, their history will be randomized from the char_jobDatabase.xml or char_historyDatabase.xml file(s) instead.*
* Reason = This specific character's reason for travel. If this field is left empty or missing, their reason for travel will be randomized from either the char_jobDatabase.xml or char_reasonDatabase.xml file(s) instead.*

The string "\n" can be used in the History or Reason field to display a line break. DO NOT use this in any other field.
