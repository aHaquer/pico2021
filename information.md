# information

This challenge was the worst bullshit.
To susie, I would like to personally say, "fuck you."

> Files can always be changed in a secret way. Can you find the flag? cat.jpg

We can use exiftool to see the metadata

> exiftool cat.jpg

Returned we get

ExifTool Version Number         : 10.80
File Name                       : cat.jpg
Directory                       : .
File Size                       : 858 kB
File Modification Date/Time     : 2021:03:17 00:01:01-05:00
File Access Date/Time           : 2021:03:17 00:01:26-05:00
File Inode Change Date/Time     : 2021:03:17 00:01:08-05:00
File Permissions                : rw-rw-r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1

For some reason someone thought that layering yet another challenge with base64 was a good idea, so the flag is the base64 decode of "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9"

**picoCTF{the_m3tadata_1s_modified}**