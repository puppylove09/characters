Characters
==========

Each of the XML files in this directory correspond directly with the Database files used in the game. Please use caution when editing old characters or adding new ones, as a mispelling of any of the node names could cause errors in the game.

char_nameDatabase.xml
==========
The char_nameDatabase.xml file is used to generate the general Character data, as well as optionally used to generate all other data as well. This file is extremely flexible as it allows the simple generation of simple names, gender, and nationality, or the creation of the entire backstory and occupation of a character. It does not, however, allow the customization of any character's clothes, as that is entirely randomized based on Gender and Nationality.

Here is an example structure of this XML file containing a full character's data. Note that some of this information is optional. See below for descriptions of each node.
~~~
<Info>
	<Name>Ron Swanson</Name>
	<Gender>0</Gender>
	<AgeMin>20</AgeMin>
	<AgeMax>40</AgeMax>
	<Nationality>0</Nationality>
	<Hometown>Pawnee</Hometown>
	<Job>Parks &amp; Recreation Officer</Job>
	<History>Hates people\nHates everything</History>
	<Reason>Wants to get as far away from people as he can</Reason>
</Info>
~~~
These are the fields that can be used for this file.

* Name = Name of the character, to be displayed underneath them and in their Travel Visa.
* Gender = An int of their specific gender. (0 = Male, 1 = Female)
* AgeMin/AgeMax (Option) = An int value used to randomize their age between the two values. If a specific value is desired, simply set these two valeus to be the same value. If these two fields are left empty or missing, their age will be randomized from the char_jobDatabase.xml file instead. If these two fields are missing from the Job Database, their age will be randomized between the ages of 18 (Adulthood) and 65 (Retirement). If only AgeMin is used, a random number is generated between AgeMin and 65 (Retirement). If only AgeMax is used, a random number is generated between 18 (Adulthood) and AgeMax.
* Nationality = An int of their specific nationality. (0 = American, 1 = Wild West, 2 = Canadian, 3 = European, 4 = Asian, 5 = Russian)
* Hometown = The name of this specific character's hometown. If this field is left empty or missing, their hometown will be randomized from the char_jobDatabase.xml instead.
* Job (Optional) = This specific character's job. If this field is left empty or missing, their job will be randomized from the char_jobDatabase.xml file instead.
* History (Optional) = This specific character's history. If this field is left empty or missing, their history will be randomized from the char_jobDatabase.xml or char_historyDatabase.xml file(s) instead.
* Reason (Optional) = This specific character's reason for travel. If this field is left empty or missing, their reason for travel will be randomized from either the char_jobDatabase.xml or char_reasonDatabase.xml file(s) instead.

The string "\n" can be used in the History or Reason field to display a line break. DO NOT use this in any other field. The Ampersand symbol (&) can be used by inputting "&amp;".
