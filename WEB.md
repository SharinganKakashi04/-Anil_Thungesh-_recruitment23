## HTML 
i started learning HTML from codeacademy, and leanred about the basic syntax and learned the uses of them mainly from google.
some basic tags that i learned

1. body tag..< body > used to specify the content in the HTML page
2. paragraph tag..< p > used to write a paragraph
3. html tag...< html >, used at the start of html page
4. image tag...< img > must contain src(source attribute), whose value is to output a image URL
5. doctype tag..< !DOCTYPE > must before starting html code
  , etc, and with the help of these i was able to build a simple portfolio

## CSS
- used codeacademy to learn
- css is basically used to modify the style of the site, can be used in html
- 

# PICOCTF:
## Powercookie:
- first i read about cookies and their functions, then leaned how to mmodify them
- opened the the website given the the task and then inspected, which gave me access to the html and css code
- then in Application tab > cookies > i was able to see that the value of the cookie was 0, which means it is a false value
- once i changed the valule to 1 and refreshed the page, i got the flag

## SQL Direct:
- first i connected to the sql link provided in the question and entered the pasword and got in
- using help command i was able to see different commands that i can use
- so to modify a database, i need a command that could list the database and that was \l and \c makes us select our database as pico
- dt listed all the tables in the database, which showed flag as one of them
- and after using select * from flags, i got the flag

## Java code analysis
- downloaded the souce code and accessed the folder, under the pico folder, found the code
- found script generator, then logged into the site given and user and password
- after using this i was stuck, i was not able to proceed
