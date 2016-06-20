curl is a command line application that allows to transfer files using differnet protocols.
It does someting similar to what a browser does but from the terminal.



Examples:

navigate to a website
curl http://www.google.com
this will not open a browser but show you the server response in the terminal

save curls output into a file
$ curl -o mygettext.html http://www.gnu.org/software/gettext/manual/gettext.html

download a file in current folder
curl -O http://www.stockvault.net/data/2010/02/04/113039/small.jpg

download multiple files
$ curl -0 http://www.domain.com/{one,two,three}.txt

check in the dictionary for word
curl dict://dict.org/d:bash

One useful  way to use curls is to test your api query. the option -X allows to tell you what type of request you are doing
curl -X GET http://www.google.it
curl -X POST http://www.google.it
if you dont specify anything as in the first example curl defaults to GET

TUTORIAL - make a post request on a dummy server


try a POST request

//server that accepts post and put requests
http://posttestserver.com


The endpoint to make a post request is 
http://posttestserver.com/post.php

pass the variable dir to save in a specific folder the beginning of the parameters is market by a question mark
http://posttestserver.com/post.php?dir=myfolderName


to pass the values that you want to save use option -d of curl. try to write the curl command by your self. the solution is just few lines below 

curl -i -X POST http://www.posttestserver.com/post.php?dir=myDir -d '{"value":"my message"}' 
now you content is saved in the folder. to access it use the link provided in the response message


