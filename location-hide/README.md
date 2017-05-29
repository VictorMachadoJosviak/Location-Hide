## *NEW*  Version 1.2.5  
I'm pleased to announce that Version 1.2.5 works with almost every scenario!  
  
## Difficult Level  
3/10 even if you never used node.js  
  
  
## For what is this plugin? - Short Answer  
At the moment you can hide src="", href="", content="" values with javascript. Maybe future releases will include more like id and class!  
You import as example your index.html or every other file that fs can read and then you get a crypted index.html & external js include file.  
src="", href="", content="" will be replace with data attributes and get load via javascript.  
Invisible in source code and inspect source code*Read IMPORTANT 2 KNOW  
Even if you can reverse it you can protect your website for people searching manually for explotits because of obfuscation.  
It will be harder for attackers.  
  
created by Dennis Demand - www.hornyfamily.online  
  
This work is just for my portfolio at upwork. Everything from my side is CC0 (FREE PRIVATE & COMMERCIAL USE WITHOUT BACKLINK ) :)  
  
I´m open for jobs please contact me at upwork.  
  
https://www.upwork.com/freelancers/~01cef724ff3d3b3988  
  
  
## IMPORTANT 2 KNOW  
Current no PHP support for codes like  
```  
href="<?php echo $home; ?>"  
```  
  
  
  
You can´t hide your javascript code 100% because you send it to the user when he opens your website. But this script will hide the src=""  
part from the source code & also from the inspect code + add obfuscation. But if you search deeper you will find the js files.  
Also if you try to protect your js files with .htaccess it will not work because the user have to get to js code if you want that he can use it.  
  
This means the only option you have is to run obfuscation scripts on your js scripts + minify or other compression tools.  
You can run multiple obfuscation + copy the script 100x times inside the script or stuff like that.  
I will release in future a professional obfuscation solution.  
  
In fact you cant hide or protect your code if the user has to get it!  
The only method to protect your script is to run it manually and then send the generated data to the user.  
  
  
## For what is this plugin? - Long Answer & How to  
  
Good 2 know before start:  
Place all your scripts that you want to protect into a folder at the root of your website as example dir name _  
  
Because before you have maybe  
```  
<script src="secret/test/folder/sample.js" type="text/javascript"></script>  
```  
  
And after you have  
  
```  
<script src="_/sample.js" type="text/javascript"></script>  
```  
  
1. You have all file in 1 folder and you can make easier htaccess settings for this.  
2. You dont give the user informations about your website path structure if he is searching exploits.  
  
_______________________________________________________________________________________  
  
You import as example your index.html or every other file that fs can read and the output will be like this:  
  
  
Before:  
```  
<script src="_/sample.js" type="text/javascript"></script>  
```  
  
After:  
```  
<script data-wchIyvpKUkArTeyUIZsCekKZRROZZzMNErjvtdIqWGkytjDyhJ="bCCnkxHMRCbEnVtvOWxOqBtKgsYkZEmWzPKybVKvJktkXTWDnc" type="text/javascript"></script>  
```  
  
  
  
Then in a external js file you can add the generated jquery code that will be generated in a external file:  
```  
$(document).ready(function() {  
var qRlhGXpAjYCmwyVlAnbJmUABkGzIavYdkcVArRvICzLhaeJbbV = document.querySelectorAll('[data-wchIyvpKUkArTeyUIZsCecKZRROZZzMNErxvtdIqWGkytjDyhJ="bCCngxHMRCbEnVtvOWxOqBtKgsYkZEmWzPKybVKvJGtkXTWDnc"]');  
$('[data-wchIyvpKUkArTeyUIZsCecKZRROZZzMNErxvtdIqWGkytjDyhJ="bCCngxHMRCbEnVtvOWxOqBtKgsYkZEmWzPKybVKvJGtkXTWDnc"]').attr("src", "_/sample.js");  
$('[data-wchIyvpKUkArTeyUIZsCecKZRROZZzMNErxvtdIqWGkytjDyhJ="bCCngxHMRCbEnVtvOWxOqBtKgsYkZEmWzPKybVKvJGtkXTWDnc"]').attr("src", "");  
});  
```  
  
The js file will be loaded and then the src path will be deleted. This step deletes the src path from the source code.  
The delete step will only be used at src.
For me it works for canvas animation and other stuff. Maybe it will not work for live scripts.
If you found bugs please contact me at upwork. 
  
  
  
## IF YOU DONT DO THIS - YOUR CODE WILL NOT WORK  
This module needs uncrypted jQuery + include codes for correct working this means in example:  
  
```  
<script src="/common/jquery.min.js" type="text/javascript"></script>  
<script src="/common/included_jquery_codes.js" type="text/javascript"></script>  
```  
  
That you need to import these both scripts in the normal way like you always import external js files. In this case the included_jquery_codes.js include the generated jquery include codes. It is very important that these scripts will be loaded before everything else. Most important jQuery :)  
  
  
## FEATURES  
If you name your external file where you import the generated code "______________.js"(without quotes)  
and if you call your jquery file "jquery.min.js"(without quotes),  
then the script will automatically not crypt and not use those both js files. This means you don´t need to do it manually :)  
  
  
  
## Installation  
  
Step 1: Install plugin with  
  
```  
npm install location-hide  
```  
  
Step 2: Install this plugins and include it on your file  
  
```  
const location_hide = require('location-hide'),  
      path = require('path'),  
      filePath = path.join(__dirname, './index.html'), // <-- FILE IMPORT HERE  
      fs = require('fs'),  
      randomize = require('randomatic'),  
      simpleTimestamp = require('simple-timestamp');  
```  
*IMPORTANT*  
If you want to change the const names you need to change them aswell in node_modules\location-hide\index.js  
  
  
Step 3: Use  
```  
location_hide();  
```  
to start the module. Just paste it under the const code before.  
For custom changes please look at node_modules\location-hide\index.js  
  
  
  
## Where are my generated files?  
The files will be exported to the root of your node.js script that runs the convert.  
  
  
  
## License  
MIT - created by Dennis Demand - www.hornyfamily.online  
You can do what ever you want with this script:) If you want to support the backlink to www.hornyfamily.online  
