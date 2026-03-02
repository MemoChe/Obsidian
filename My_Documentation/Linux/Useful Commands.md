`-sudo pacman -Syu --overwrite '*'` =>This command will help us to remove the error that the packages could not be installed in case of removing  /var/lib/pacman folder by error.
`-cat` => print the file | => takes the parameter on the left as input
cut => is used to cut specific parts of an entry.
	`-cut -d+ : (delimiter) => cut -d: `
	`-cut -d: + -f2,3 => print fields 2-3 of the input`
	`-cut -d: --complement -f1 => extracts all fields except the first field`
	`-cut -d',' -f2,4 data.csv => extracts the 2-4 fields from a csv`

`-cat /etc/passwd | cut -d: -f1 => show us all the users in our session`

`-chown` =>  this command is used to change the ownership of files and directories.
	`-chown memo file.txt => this changes the owner of file.txt to alice.
	`-chown alice:memo file.txt => this changes the owner of file.txt to alice and the group to memo.
	`-chown -R alice /path/to/directory/ => this changes the owner of a directory and its contests.
	`-chown :memo file.txt => this changes only the group of a file.
	`-chown 1001:1002 file.txt => using id and gid.
	