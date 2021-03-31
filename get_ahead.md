# Get Ahead
 Solved by Pyrus

> Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:28916/

As Pyrus pointed out, the name GET aHEAD implies some kind of interaction with the HEAD which is a method in HTTP.

Upon googling "curl request to head" # curl sends get requests

we find that the command line flag for this is -I, making the solution

> curl -I http://mercury.picoctf.net:28916/

In response, the server sends 

> HTTP/1.1 200 OK
> flag: picoCTF{r3j3ct_th3_du4l1ty_70bc61c4}
> Content-type: text/html; charset=UTF-8

**picoCTF{r3j3ct_th3_du4l1ty_70bc61c4}**