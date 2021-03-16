# Python Wrangling 
**picoCTF{4p0110_1n_7h3_h0us3_68f88f93}**


We're given a python file, a flag file, and a password file.

To immedietly solve the challenge, we only need to read:

```python
usage_msg = "Usage: "+ sys.argv[0] +" (-e/-d) [file]"
help_msg = usage_msg + "\n" +\
        "Examples:\n" +\
		        "  To decrypt a file named 'pole.txt', do: " +\
				        "'$ python "+ sys.argv[0] +" -d pole.txt'\n"
```

Upon inspecting the python file, we can immediately figure out that in order to get out flag, we just need to run 

> python ende.py -d flag.txt.en

And then enter the password (from the password file)

> 68f88f9368f88f9368f88f9368f88f93

**picoCTF{4p0110_1n_7h3_h0us3_68f88f93}**
