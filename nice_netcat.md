# Nice Netcat
**picoCTF{g00d_k1tty!_n1c3_k1tty!_3d84edc8}**

> There is a nice program that you can talk to by using this command in a shell: $ nc mercury.picoctf.net 49039, but it doesn't speak English...

Upon netcatting in, we're shown the numbers (I've removed newlines here)
> 112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 51 100 56 52 101 100 99 56 125 10

These are clearly ASCII numbers, and using https://convert.town/ascii-to-text confirms this
**picoCTF{g00d_k1tty!_n1c3_k1tty!_3d84edc8}**