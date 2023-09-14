Cleanup and create fields:
Refer to School Demographics report instructions for these fields (Ethnicity and Gender) 

Cleanup and transform the Former School Type field (NOTE: I left in NULL schools, because not sure what we want to do with those for now, but these schools can be hidden)

Right click on Former School Type and click duplicate (this should create a field called Former School Type (copy)) (an alternative to duplicate would be right clicking and creating a calculated field)

Right click on Former School Type (copy) and rename to Former School Type (cleaned), then right click on Former School Type (cleaned) again and click Edit, then add the transformation command to Former School Type (cleaned) and click Apply, then OK

Create a calculated field called Count Former School Type (cleaned) using the command COUNT([ Former School Type (cleaned) ])

Count Students 2019-Present is auto created for you, but if not the process should be the same as this field

Create the report:
Create new sheet for By Former School Type 

Add School to Rows

Add Students 2019-Present Count to Columns

Create a calculated field called  Former School Type (cleaned) that has the below if/else command 

Add Former School (cleaned) to the Color tab in the Marks section

Right click Students 2019-Present Count (in the Columns section), then click Quick Table Calculation, then click Percent of Total

Right click Students 2019-Present Count (in the Columns section), then click Edit Quick Table Calculation, then click click on Table (across)

Highlight all bars and click Mark Label, then click Always Show

To add the different filters --- Gender (cleaned), Ethnicity (cleaned), Graduation Year, School

Right click on the field name either on the graph or in Rows, click Show Filter, then right click on the name again and click Remove

For Graduation Year, make sure to right click on it and set it to Discrete first(for both the Detail and when adding to the Rows), then click Show Filter

Extra stuff: changing bar graph colors -> right click on the Former School Type filter (on the side) and click Edit colors

Former School Type command: 
IF [Former School Type] == 'Private' OR [Former School Type] == 'Private (Catholic)' OR [Former School Type] == 'Private/Non-Catholic'

THEN 'Non-Public (Catholic)'

ELSE [Former School Type]

END
