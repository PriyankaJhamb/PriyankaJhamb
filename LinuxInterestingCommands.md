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

### Reference:
- [https://youtu.be/19mmVar-s5Y](https://youtu.be/19mmVar-s5Y)
