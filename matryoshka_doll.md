Description:

Solved by Skuzi

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: this

With this room we are given a jpg file with files within files, refrenced by the dolls within dolls.
To extract these files I used binwalk -e doll.jpg, its pretty self explanitory, just used this command to extract the files hidden. 
I had to extract 4 different dolls before I got to the end. At the end of the dolls I was greeted with a flag.txt file.
While I couldnt just open the file because the characters were question marks and a bunch of weird akward stuff that certainly wasnt a flag.
I popped the flag.txt file into cyberchef and the output was: p.i.c.o.C.T.F.{.b.f.6.a.c.f.8.7.8.d.c.b.d.7.5.2.f.4.7.2.1.e.4.1.b.1.b.1.b.6.6.b.}
I just removed the periods and the submitted the flag.
Flag: picoCTF{bf6acf878dcbd752f4721e41b1b1b66b}
