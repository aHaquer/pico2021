# Scavenger Hunt

> There is some interesting information hidden around this site http://mercury.picoctf.net:55079/. Can you find it?

So we have been told a website with information hidden, so the first thing I did was checked the source code of the page.

From the source code I noticed the first part of our flag: (part1) picoCTF{t

Also from the source code we can see we can access the "mycss.css" which leads us to part 2 of the flag: h4ts_4_l0

As I was looking around the webpage I started up gobuster to check for directories, gobuster picked up on /robots.txt
from /robots.txt we are greeted with part 3 of our flag: t_0f_pl4c

I found part 4 of the flag by using gobuster with the common.txt wordlist: 3s_2_lO0k

The prompt to find part 5 of the flag had to do with storing lots of information so I googled mac database files and came up with the conclusion .ds_store: _74cceb07}
