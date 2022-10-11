## PIPE '|' Command
``` ls | wc -l ```
- Output of ls acts as input to wc
- This command gives us the number of files in the directory in which we are.
- Multiple commands can be connected in this way forming a pipeline in which former gives output and it will be used as input to the latter command.

## Tee command
- tee command reads the standard input and writes it to both the standard output and one or more files.

``` ls | tee list```
- Output of ls is given as input to the tee command and tee command writes the input in the list file and then also gives or displays the same output.

## wc command 
- which gives us the word counter/ files counter depending on the input
```ls |wc -l```


## Flags (or OPTIONS)  
Flags are used to modify the behavior of a command. For example ls -a, -a tells the ls executable to list all files in the directoy, including hidden ones. Flags are also called OPTIONS.

## [Use of - or --](https://www.ibm.com/docs/en/aix/7.1?topic=names-command-flags)
- is to tell that this is a flag.
-- is to tell that this is a parameter not flag.


### Reference:
- [https://youtu.be/19mmVar-s5Y](https://youtu.be/19mmVar-s5Y)
- [https://docs.lug.oregonstate.edu/Linux/basic-commands/#:~:text=Flags%20are%20used%20to%20modify,Flags%20are%20also%20called%20OPTIONS.](https://docs.lug.oregonstate.edu/Linux/basic-commands/#:~:text=Flags%20are%20used%20to%20modify,Flags%20are%20also%20called%20OPTIONS.)
