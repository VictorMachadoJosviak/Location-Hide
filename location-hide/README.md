## FSIG(Fake Script Include Generator) added to Version 1.4.1  
For more Information please look at: Long Answer & How to  
For Live DEMO look at the source code the crypted sample page link below. You will find the code before the  
```   
</body>  
```  

Inside of this jungle from fake include scripts is the real include js file which was generated from this module.  

## Live DEMO  
I created this before and after preview for you with a sample free website template. Please read the text below to understand what you can hide and what not. Also dudes I offer you this script complete for free + updates so please don´t try to damage/attack the preview server. Thank you for understanding.   
  
*KNOWN BUGS*  
Please notice that this preview pages got sample advertisement popunder to show you that you can also include those kind of scripts.  
But the problem is those scripts will open before everything else and can crash the load of your js files. DON`T BE SCARED the following problem will only caused by some scripts in this example the popunder code. If I would remove this popunder code everything would be normal again. This maybe will happen to you with other js scripts aswell(Maybe you can make timeouts on your scripts to workaround this). But this only happens when you never visited the site and your cache is empty. After refresh everything will work. On this live demo you can see it if there is no close button when you open a image + missing effects. You will see it!  
If you want to workaround this you need to refresh the page after the user open your site. You can easy do this with javascript/jQuery.  
Then set a cookie that this will be only done once. You can make a cool ajax loader or something that users don´t think hey why is my site loading again :)  
  
Also you should never input your advertise code before the crypt process, because maybe you crash your advertise codes with this!  

Original Website Template [DOWNLOAD]:  
https://templated.co/visualize
  
LIVE DEMO ORIGINAL:  
www.forbiddentube.online/samplepage/original
  
LIVE DEMO CRYPTED WITH LOCATION HIDE:  
www.forbiddentube.online/samplepage
  
The domain above contains sexual content and should be only viewed by persons over 18 years! 
  
  
## *NEW*   Version 1.4.1  
I'm pleased to announce that Version 1.4.1 works with almost every scenario!  
This is a ongoing project. Stay tuned for updates 
  
Added:  
• FSIG(Fake Script Include Generator)  
• .jpg was added to src section  
• id="" + class="" UPDATE  
• src section updated, should now work with almost everything + iframes 
  
Fixed:  
• Added .delay( 10000 ); to every src delete event to dodge load bugs - more information below  
  
## Difficult Level  
3/10 even if you never used node.js  
  
  
## For what is this plugin? - Short Answer  
At the moment you can hide src="", href="", content="", id="", class="" values with javascript.
You import as example your index.html or every other file that fs can read and then you get a crypted index.html & external js include file.  
src="", href="", content="", id="", class="" will be replace with data attributes and get load via javascript.  
Now also with obfuscation of all your data attributes + FSIG(Fake Script Include Generator).  
Invisible in source code and inspect source code*Read IMPORTANT 2 KNOW  
Even if you can reverse it you can protect your website for people searching manually for explotits because of obfuscation.  
It will be harder for attackers.
 
created by Dennis Demand 
  
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
If your js scripts use css selector or jquery selector like $('#sample') then you need to change this to the generated data value  
  
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
$('[data-wchIyvpKUkArTeyUIZsCecKZRROZZzMNErxvtdIqWGkytjDyhJ="bCCngxHMRCbEnVtvOWxOqBtKgsYkZEmWzPKybVKvJGtkXTWDnc"]').attr("src", "").delay( 10000 );  
});  
```  
  



Since Version 1.4.1 is FSIG(Fake Script Include Generator) part of this project.  
This nice tool allow you to add fake include scripts. As example  
```  
<script src="_/Dniw94XqAh6v69sMOy3PlajC0WlMZASgxs37FlnVcW5cX4k8vuwLTcyD3tWYxZPH1OBxRrnFRtKVf5bXbd24rNcdVfWNuBrhvaMl.js"></script>  

<script src="_/TXCRCSq5xo335CGmApFbqWggJuiZmIzuPXGgHKWuQljXqIvKSdVeO4qNUmTcaIRlVpZ0wfA6h1I9MviVOs0KiD7bdRgNYiSy3gUD.js"></script>  

<script src="_/vYmuX2f5tY3L0WGIBclT5j1qWyF2g5bEj026ZW90HzIaCMFjneLB2lYmofRbMy51YKXuiMbhNmNICKSk99OS6yoTTly2wAWVGQMp.js"></script>  

```  
This code will be paste at the end of your crypted file. You should cut it out and paste it directly before your  
```   
</body>  
```  

WHY IS THIS USEFUL?  
Because now you can hide your external generated js file in this jungle of include codes. Just rename your all your files that you want to hide. Of course you should use the same character length for this. Just copy and change 2 or 3 letters.


To avoid that attackers bulk download all scripts. I cant create empty script codes here, because then you can delete all 0KB scripts. You can also try to change the randomize values in the module index.js to generate different sizes for your fake scripts or change the content of your fake scripts.(I will offer in future a professional obfuscation solution for this stay tuned!)  
Location Hide will create this files in the folder ./FAKE_SCRIPTS_EXPORT_AREA/ from the root of your path where you started the script  

*LONG LOADING TIMES*  
The default is 100 fake include scripts. The loading time is normal with this lineup. If you got problems then reduce the amount. If you got good servers and want better protection then increase the amount.


You can define how much fake scripts you want with this const - please look bellow at installation guide 
```  
Loop_Length_fake_include_scripts = Number('100');  
```  

*IMPORTANT FOR CRYPTED JS FILES*  
I use at the moment delay of 10000 to dodge loading bugs. Maybe you need to put it higher for some server or scripts or lower if it takes too long for you. If you need to upgrade the delay time then you can add a ajax loader or something like this until the delay is over.  
  
The js file will be loaded and then the src path will be deleted. This step deletes the src path from the source code.  
This will be done on every supported attribute of the script.  
For me it works for canvas animation, other stuff. Maybe it will not work for live scripts.  
THIS STEP ONLY WORKS FOR JS SCRIPTS! This will be not done for the other attributes like href.  
If you found bugs please contact me at upwork or wrote a comment at github.   
  
  
  
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
const location_hide = require('location-hide');  
      path = require('path'),   
      filePath = path.join(__dirname, './index.html'); // <-- FILE IMPORT HERE  
      fs = require('fs');  
      randomize = require('randomatic');  
      loop = require('serial-loop');  
      Loop_Length_fake_include_scripts = Number('100'); // <-- CHANGE AMOUNT OF FAKE INCLUDE SCRIPTS HERE
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
The fake include codes will be at in this folder also at the root ./FAKE_SCRIPTS_EXPORT_AREA/  
  
  
  
## License  
MIT - created by Dennis Demand - upwork.com/fl/dennisdemand

Please contact me on Upwork when you need custom Software!
