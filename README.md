# PriceCalc

I made this program for running a store on a minecraft server. I wanted to base my prices off of server prices and other stores, but at the time the only items with prices were the basic materials. Instead of calculating out the prices by hand every time I added a new item or server prices changed, I decided to write this program.

This program lets you calculate out shop prices easily for different base material cost and new items. It works by using the item recipes to figure out how many raw materials an item needs, then figure out the price from the raw material costs. The program also stores all the item data in a text document for later use. You MUST use the "exit" command to save the item info before closing the program.

The program currently allows for 5 commands:
* "add" - lets you add an item to the list. Follow the prompts and you should be good
* "price \<item name\> - returns the price of the specified item
* "list" - lists all currently stored items in alphabetical order
* "change" - goes through all raw material prices and allows you to change any of them (plan to make it so you can change one item's value)
* "exit" - exits the program and saves item recipes/prices
  
When adding an item that must be crafted, you will be asked for 2 things:
* how many of the item its recipe produces (example: fluix crystals are 2, glass panes are 16, sandstone is 1)
* the recipe for the item. The format for recipes is a comma-separated list of the component item name and the amount needed
		(example: recipe for 1k storage cell is "certus quartz, 4, redstone, 4, logic processor, 1"

To run this program, simply download the 2 java files and run Engine.java. 
For those curious: Item.java is the class that does all the heavy lifting for price calculations, saving/loading the item set, and so forth. Engine.java runs the program by getting the user input and using the input to call different methods inside Item.java.

NOTE: This program is very picky and typos will cause it to think it is a new item. All item names must be spelled consistently (i.e. referring to certus quartz as "certus" means you must type "certus" for the program to recognize it.)

**If the program throws any errors or you find a bug, please let me know what happened and copy the program output so I can trace it back and test it myself. This code is still a work in progress and I'm sure I missed multiple errors that the program will need to handle.**
