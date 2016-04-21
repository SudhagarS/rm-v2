# rm-v2
Rm-v2 overrides the system 'rm' program with a better version. Rm-v2 doesn't delete files immediately. Instead the 
files are kept in **~/.rm-bin** directory and can be restored if required. With this, you don't have to worry about running 'rm -rf'
on a important directory. You can restore the last removed file/directory with **'rm --undo'**.


## Installation

To install rm-v2, paste and run the following commands in your terminal.

    git clone https://github.com/SudhagarS/rm-v2/
    
    sudo mv rm-v2/rm /usr/local/bin/
    
    chmod u+x /usr/local/bin/rm
    
To remove the downloaded files once installed run
    
    rm -rf rm-v2
    
    
## Usage

To remove a file or a directory

    rm filename  - To remove a file
    rm directory/* - To remove all files in a directory
    rm directoryname- To remove a directory
    rm hello* - To remove a set of files with a common prefix
    

Note: All removed files are sent to ~/.rm-bin. ~/.rm-bin is cleaned after every remove if the number of files 
there exceeds 20.


Options

    rm --undo - To recover the last removed file or directory
    rm --clean - Clears the ~/.rm-bin directory.
    rm --uninstall - To uninstall rm-v2 and go back to system 'rm'.
    
