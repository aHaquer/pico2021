# Weird File Writeup

> What could go wrong if we let Word documents run programs? (aka "in-the-clear"). Download file.

I have no fucking idea what in-the-clear means, but I do know that Word docs run macros in the background 
sometimes. The DefCon talk in the hint also suggests thats the issue. (https://www.youtube.com/watch?v=Y7IJjnLGqTQ)
After you watch the talk (or skim) you'll notice the presenter gives a tool to view Macros running in a word doc
without owning word or without opening the doc (Which I don't, and opening something you know to be generally 
malicious is bad practice)

Using the command 

sudo pip install -U oletools
You'll install the package necesarry for examining the word doc.
Running the command 

olevba -c weird.docm

Will give you the following

===============================================================================
FILE: weird.docm
Type: OpenXML
WARNING  For now, VBA stomping cannot be detected for files in memory
-------------------------------------------------------------------------------
VBA MACRO ThisDocument.cls 
in file: word/vbaProject.bin - OLE stream: 'VBA/ThisDocument'
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 
Sub AutoOpen()
    MsgBox "Macros can run any program", 0, "Title"
    Signature

End Sub
 
 Sub Signature()
    Selection.TypeText Text:="some text"
    Selection.TypeParagraph
    
 End Sub
 
 Sub runpython()

Dim Ret_Val
Args = """" '"""
Ret_Val = Shell("python -c 'print(\"cGljb0NURnttNGNyMHNfcl9kNG5nM3IwdXN9\")'" & " " & Args, vbNormalFocus)
If Ret_Val = 0 Then
   MsgBox "Couldn't run python script!", vbOKOnly
End If
End Sub

Obvious Base64 string is obvious
Run the command 

echo cGljb0NURnttNGNyMHNfcl9kNG5nM3IwdXN9 | base64 -d 

Get Result:
picoCTF{m4cr0s_r_d4ng3r0us}  