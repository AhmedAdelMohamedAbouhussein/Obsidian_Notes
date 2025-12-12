	~ === home/user
	. === current directory 
	.. === pervious directory 

inside the root (/)
	- /mnt === disk
	- /home === users
	- /var === variables
	- /bin === binary files

file access  {  _    __ __ __    __ __ __    __ __ __  }
	
	_ === file ( _ ) or directory (d)
	
	_ _ _    _ _ _    _ _ _  === permissions (read / write / execute)
	 root    group     user
commands
	- cd (change directory )
	- ls path (list all directory content) (-l long description) (-a view hidden content)
	- pwd (print working directory)
	- clear (clear the terminal)
	- history ( view all command history you typed)
	- touch filename . extension  change file timestamps
	- nano filename . extension (write in a file) (text editor)
	- cat filename . extension (concatenate and display content in a file)
	- echo (print)
	- echo text >> filename append to file (append to a file)
	- >> append 
	- > clear and write  (overwrite)
	- grep
	- rm (remove a file)
	- man (manual to view commands descriptions arguments , etc.) 
	- lahex (display with color)
	- chmod
	- cp
	- mv
	- wc
	- wget
	- mkdir
	- rmkdir
	- sudo
	- 

arguments
	- l (long description)
	- a (view hidden content)
	- la (view long description with hidden content)
	- rm (-rf) recursive remove
	- Aal (display long description of all hidden files except ( . .. ))


add(x , y) //arguments
add (int x, int y) //parameters 


assignment create file that gets deletes after 1 hour

1)  | pipe to create a channel
	1) ls | cat >> all.log
	2) python.server.py | cat >> all.log or ls > all.log
	3) echo "Ahmed Adel" >> all.log 
2) touch f{1..10}.se
3) ls && rm *.se

ls std output
echo text input
cat std input and changes to text output

sudo = super user do. command gets root permission 

.sh = executable file for linux

bash scripting is a **interrupted** language (scripted language)

(she bang) pointer to interpreter 
she bang  symbol : #! -> /bin/bash (interpreter_path)


chmod +x (filename) 
chmod 777 (filename)
u +x
G +x
r +x

run file: 
	1) ./filename    //terminal works on file
	2) bash bash1.sh  //bash command works on file