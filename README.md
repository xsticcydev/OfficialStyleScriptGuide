# Official Roblox Style Script Guide


https://www.roblox.com/library/6149121433/StyleScript

*(If you haven’t installed the plugin yet, install it first!)



## Basic level

**Open the script editor:**
1) Go to the ‘Plugins’ tab \
![image](https://user-images.githubusercontent.com/50070707/103181816-a6318900-48a5-11eb-8663-1541e9e99625.png)

2) Click on the ‘Script Editor’ button \
![image](https://user-images.githubusercontent.com/50070707/103181822-c19c9400-48a5-11eb-817a-a9d3dae90e08.png)

3) The script editor should show up now \
![image](https://user-images.githubusercontent.com/50070707/103181827-c9f4cf00-48a5-11eb-9f48-0c96e3638be8.png)

**Create your first script**
   Type:
   ```
   _btn:default
   bg:(255,200,200);
   end _btn:default
   ```
   What this code does?
   It sets the background color of all TextButtons to the RGB color 255,200,200
   
   How this code built up?
   
   **The first line**
   
   In the first line we have a *definition*. All *definition* starts with a _ symbol
   
   After the _ symbol comes the class of the objects we want to style. In this case the TextButtons.
      Then why don't we write TextButton instead of btn?
      You can write both TextButton and btn. They are the same. At the bottom of this guide there is a list of all 'shortcuts' in StyleScript.
   
   Next we have a : symbol and after that we have the *state*
   We have three states in StyleScript:
      default
      hover
      active
   Also, we can write them down with numbers too:
      0,
      1,
      2
   
   **After the first line**
   
   After the first line, the *properties* come in.
   There are a lot of properties we can change, in this case we change the background color.
   
   Before the : symbol we have our *property*. (List of all the properties and their 'shortcuts' at the bottom of this Guide)
   
   After that we have our *value*. In most of the cases it's just a number or a string.
   But in this case we have a RGB value. The syntax of a RGB value is: (r(0-255),g(0-255),b(0-255))
   
   After the *value* we need to put a ; symbol at the end of the line.
   
   **The last line**
   
   In the last line we close our *definition*.
   To do this we write: 'end (definition)'
   For example:
   ```
   _frame:hover
   
   end _frame:hover
   ```
   See? We just wrote 'end ' + *definition*
   
**See an example of longer code**
```
_btn:default
bg:(255,255,255);
end _btn:default

_btn:hover
bg:(255,200,200);
end _btn:hover
```
Do you understand this code?
If don't, please read the guide again.
If you do understand the code you can try yourself at the Advanced Level StyleScript

## Advanced Level
(Warning: at advanced level styling we will use 'shortcuts'! You should read them before learning Advanced Level)
**Statements**
Yes, you heard it right! We can have statements in our styles!
See an example:
```
_btn:default $OFFSET_SIZE_X > 200
bg:(255,0,0);
end _btn:default
```
What this code does?
It changes all of the TextButtons background color to the RGB color 255,0,0 IF the button's offset(pixel) size on the X axis is bigger than 200
Okay, what happens here?
We will only focus on the first line.
First, always write our statement after a $ symbol!
**How to build up a statement?**
```
OFFSET_SIZE_X > 200
```
First we have our *statement property*.
After we have the *statement type*.
And last we have the *statement value*(anything).
So we check of the offset(pixel) size on the X axis is bigger than 200 then we approve the styles on the object. \
**Statement properties**
* NAME (the object's name)
* Z_INDEX (the object's ZIndex)

* OFFSET_SIZE_X (the object's offset(pixel) size on the X axis)
* OFFSET_SIZE_Y (the object's offset(pixel) size on the Y axis)
* SCALE_SIZE_X (the object's scale size on the X axis)
* SCALE_SIZE_Y (the object's scale size on the Y axis)

* OFFSET_POS_X (the object's offset(pixel) position on the X axis)
* OFFSET_POS_Y (the object's offset(pixel) position on the Y axis)
* SCALE_POS_X (the object's scale position on the X axis)
* SCALE_POS_Y (the object's scale position on the Y axis) \

**Statement types**
* = (if *statement property* is equal to *statement value*)(for any)
* > (if *statement property* is bigger *statement value*)(for numbers)
* < (if *statement property* is less *statement value*)(for numbers)
* contains (if *statement property* contains *statement value*)(for strings)

## Shortcuts
* **Properties**
* bg : BackgroundColor3
* border-color : BorderColor3
* border-size : BorderSizePixel
* **Classes**
* button : TextButton
* btn : TextButton
* input : TextBox
* lbl : TextLabel
* label : TextLabel
* imglbl : ImageLabel
* imgbtn : ImageButton
* **States**
* 0 : default
* 1 : hover
* 2 : active
