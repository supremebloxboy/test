pyinstaller --onefile -w file.py
pyinstaller -i ico.ico --onefile -w file.py


Bugs:
binery converter


Information:
This program is seperated into 2 parts, the program part, and the roblox part.
The programs takes an image and stores it's information (i.e., The width and height of the image, the color, transparency and location of the pixels), and stores it in a text file.
Thats part 1, Then you take that information and put it into roblox and it will rebuild the image from the data.

How to use:
1. First you run the "ImageToText" program, after you run it, it will ask for a picture, after you select the picture,
   it will take the picture and store the info in a text file, the text file is stored in the same directory as the program,
   The text file should open automaticaly when it's done, if it hasn't opened, you have to just wait or try again, bigger images take longer.

2. after you get the text file, you have to give it to the roblox script, you have 3 option,
   1. post it on github and put the link in the script, and change the "Load_From_GitHub" value in the script to "true".
   2. post it on pastebin and put the link in the script, and change the "Load_From_Pastebin" value in the script to "true".
   3. copy and paste the text file directly into the script, put it into the "imageData" value in the quotes, Example, imageData = "Text_File_Data_Here"

3. After all that run the game, the script will build the image, after its done, copy the image then stop the game, and paste it in the game, Done.
   you can also have the game just build the image everytime you play, but that might cause alot of lag.

Debugging/Errors:
1. Make sure you're not using multiple methods of providing the pixel data, like using pastebin and string value and pasting the link in the script.
   Please only use one method, Set the method that you're using to true inside the script and the other methods to false.
2. If you're using the string value method, make sure the name of the string value is "ImageData", and make sure it's inside of the script object.
3. If you have any script errors (To Check, Open the "Output" window by clicking the "VIEW" tab at the top of studio and enabling "Output"),
   Scripting Errors may include, Using an unsuppored file type(Only png, bmp, dib, jpg, jpe, jpeg is supported),
   Improper Formating of the pixel data, pixel data should look like this, [[240,240],[129,127,55],[255,255,255],[0,0,0]],
   the first [240,240], is the width and height of the image, the rest are the RGB values of the individual pixels,
   sometimes there's a fourth value representing transparency of the pixel, [[240,240],[129,127,55,255],[255,255,255,0],[0,0,0,255]],
   0 is transparent, 255 is fully visible.
   Also if the RBG of the pixel is the same, the script will shorten it to just the 1 value for RGB, so [[240,240],[55,55,55,255],[255,255,255,0],[0,0,0,255]], Becomes [[240,240],[55,255],[255,0],[0,255]]
   Same goes for transparency, if the image has no transparency, the transparency value will be omitted, [[240,240],[132,0,55,255],[111,255],[0,255]], Becomes [[240,240],[132,0,55],[111],[0]]

Limitations:
Pastebin has a 512kb file limit which is a image about 250x250
GitHub is 25mb, which is about 1920x1080
In-script is just about whatever your pc can handle, the bigger the image the more characters the more lag


If you have any questions message me on roblox, supremebloxboy, or email me at supremebloxboy1@gmail.com