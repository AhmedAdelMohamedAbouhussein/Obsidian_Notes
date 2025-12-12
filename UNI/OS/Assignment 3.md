list all files and color the wanted one in green using grep

	
	ls | grep --color=always lab2.se
	

- **`ls`** → lists all files and folders in the current directory.
- **`|`** → sends the output of `ls` as input to the next command.
- **`grep`** → searches for text patterns in the input it receives.
- **`--color=always`** → makes matching text appear in color (green by default).
- **`lab2.se`** → the pattern `grep` looks for and highlights in the results.