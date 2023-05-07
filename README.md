Download Link: https://assignmentchef.com/product/solved-inventory-program
<br>
Take another look at the Item class we created in lab 11. (File is located on Blackboard.) We will add some additional stuff to this.

//lab11

class Item{

private String description;

private int quantity;

private double price;

public Item(){

description = “Empty”;

quantity = 0;

price = 0;

}

public Item(String description,double price){

this.description = description;

this.quantity = 0;

this.price = price;

}

public Item(String description,int quantity,double price){

this.description = description;

this.quantity = quantity;

this.price = price;

}

public void setDescription(String description){

this.description = description;

}

public String getDescription(){

return description;

}

public void setQuantity(int quantity){

this.quantity = quantity;

}

public int getQuantity(){

return quantity;

}

public void setPrice(double price){

this.price = price;

}

public double getPrice(){

return price;

}

}

Make sure the class is called Item. This is your template class.

Start with what you created in Lab 11 – three instance variables, an accessor and modifier for each variable, and three constructors.

Add a static constant which is an integer and represents the minimum quantity all items should have in stock (use the value 12).

Add a Boolean method called needToOrder( ) which returns true if quantity of item is less than this minimum value (the static constant created in the previous step).

Add toString( ) which will output this way:    “Item: Lollipop   Qty: 12   Cost: $.50”

Add method called itemWorth( ) which returns current total price of the object (single object) based on the quantity on hand (qty * price)

Add method called sellSome(int) which reduces quantity of the object by the amount inputted.

Add a method called addSome(int) which increased the quantity of the object by the amount inputted.

Add an instance (not static) method called greaterThan( Item ) which returns a boolean based on whether the itemWorth of the calling object is worth more than the passed in object.

Create your driver program and call it Inventory. This class will contain your main method. (Do not use the driver program from Lab 11. Start fresh.) In this driver program, create an array of 10 Items. Use an array. Do not use a premade class such as ArrayList (or any others). The array will start empty and we will be allowing the user to add and remove items from the array. We will assume there will always be 10 or less Items in the array, and we will assume that we will always use and fill in the beginning of the array, with the remaining unused values left at their default of null. If we delete any items in the middle of the array, you must shift items to remove the empty spot. All items should always be at the beginning of the array.

For example: If the user adds four items to the array and then sells out of the 2nd item, they may choose to remove it from the array. (To delete the values saved in an object, set the object equal to null).   With the 2nd item gone, when we print the list, we will get information about the first item, then a “null”, and then information about the 3rd item and 4th item. We do not want null to be there. The 3rd item should get shifted to the 2nd spot to fill the hole and the 4th item should get shifted to the 3rd spot.

In the main program, you will create a text menu that comes up on the output screen giving the user a bunch of choices. As they pick a choice, that action will be done, feedback will be given, and then the menu will repeat to the screen again. A switch statement might be useful here.

Your menu will do the following:

list all items

-use toString on each filled array location)

restock an item

-ask user for description, find the array element and ask user how much they’re adding to the quantity and then update the quantity

-Report if not found – should not crash

add an item to the inventory

-add it at the first null location in the array

-ask the user to give the 3 inputs and then use the constructor to create one

-Report if there is not room to add another item

Sell some of an item

-Ask user for description, find array element and ask user to say how much is sold and update quantity.

-Account for uppercase/lowercase.If user types in “gum” but it’s saved in the object as “Gum”, you should still be able to match it.Do not tell them that “gum” does not exist.

-Report if not found – should not crash

Remove an item from list

-Ask user for description, find array element

-Account for uppercase/lowercase.If user types in “gum” but it’s saved in the object as “Gum”, you should still be able to match it.Do not tell them that “gum” does not exist.

-Report if not found – should not crash

-set array location to null (make sure to shift array to fix holes)

list the items that need to be ordered

-process through the array until reach null

-call needToOrder on each and show the true results

-Report if no items need to be ordered

Report total inventory cost

-search through entire array, and sum up the itemWorths

-report the total.

Report item that is worth the most

-Use greaterThan method

Clear list

-set all array locations to null

10.   End program

Test all of your menu choices, make sure to remove items in the middle of the list and check if the rest of the choices still work. There should be try/catch blocks to prevent the user from selecting something other than 1-10. There should be try/catch blocks to keep a user from entering the wrong data type for all relevant inputs. I will test very extensively, so be prepared to do so also.

Note: You will NOT be prefilling the array in your main program. Create the array and then you will allow the user to fill the array. There should be no items prefilled in the array when you turn it in. It might be helpful for testing purposes but should be removed for the final version.

Each of these programs must be done in a separate file. Name the class Item.java, and the driver programInventory.java. Name the class in each file these names as well. If you do not name these files correctly you will lose points. Both files will be dropped into the same dropbox.

Checklist

Did you:

Include a header comment in both files that contains your name and explains what the program does?

Include necessary comments throughout both files?

Indent consistently?

Remove unnecessary or redundant code or comments? (I’ve enjoyed the funny/interesting things I’ve seen in your programs, but make this final one all business.)

Name your class names/file names as directed?

Use standard convention for naming/capitalization?

Use try/catch blocks to catch all potential exceptions?

Format your money values to 2 decimal points?

Set your data members as private?

Pass in data using a variable name that is different than your private data member? (Do not do name = name; in your setters.   Use different variables.)

Make sure your methods return the specified data type?

Give feedback after every menu choice executes? (Example: If the user chooses to remove an item from the list, make sure you let them know if it was completed successfully.)

Give enough initial information to the screen so that user knows what to do?

Test your program to make sure the array is filling in gaps consistently and correctly?

Test all options of your program in various orders?

NOTE!!! The sample on the next page is just that. A sample!! I’m only showing a small part of what your program should hypothetically look like. When grading, I will test every option multiple times in random order. This should be a fully functioning inventory-like program that is easy to use and gives me reliable output. Make sure you include all requirements specified in the information above!!