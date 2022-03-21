#### Terminal Commands

Terminal commands can be used to manipulate data in different ways. Bellow are the list of the commands and an example of there uses:

- help - shows list of all available commands
- flipx - Flip the selected dataline(s) in the X-axis.
- flipy - Flip the selected dataline(s) in the Y-axis.
- offsetx - Apply an offset on the selected dataline(s) in the X-axis.
- offsety - Apply an offset on the selected dataline(s) in the Y-axis.
- showChanges - Lists the changes applied on the current report.
- cleanOffset - Clear the offset changes applied on the current report.
- cleanFlip - Clear the flip changes applied on the current report.



##### How to use

###### Getting ids of elements

Before using the commands you should look for the id of the element you wish to change. You can find it in the Tools selection as show bellow.



![](C:\Users\salar\Documents\djuli-documentation\Terminal\textInput\where to find ids.gif)



###### flipx and flipy

​	To flip the x or y axis of the datelines you must write the command in this format

​	flipx(id) id being id of element you wish to manipulate.

###### offsetx and offsety

​	To create an offset you will need to write the command in this format

​	offsetx(id,232)  id being id of element you wish to manipulate and 232 number you wish to set

​	the offset by

###### showChanges, cleanOffset and cleanFlip

​	All three of these commands do not require id and can be typed into terminal to get desired 	effect

###### 

Learn more in [ZP Academy](https://academy.zimmerpeacock.com/courses)