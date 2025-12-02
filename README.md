# Terminal_commands
Common Terminal commands related to nano

***Method 1: Using nano (Easiest & Recommended)***

Nano is a simple text editor built into most terminals. It is very beginner-friendly because it displays the commands at the bottom of the screen.

Create and open the file: Type the following and press Enter:

    Command:
    nano myfile.txt

(Replace myfile.txt with whatever you want to name your file).

Write your text: You will enter the editor interface. Type whatever content you want.

Save the file: Press Ctrl + O (that is the letter O, not zero), then press Enter to confirm the filename.

Exit: Press Ctrl + X to leave the editor.

***Method 2: Using echo (Fastest for one line)***

If you only need to write a single line of text into a file without opening an editor, use this command.

    Command:
    echo "Hello, this is my text" > myfile.txt
How it works: This takes the text inside the quotes and puts it (>) into the file myfile.txt.

Note: If the file doesn't exist, it creates it. If it does exist, this will overwrite it.

***Method 3: Using cat (Quick for multiple lines)***

This is useful if you want to type a few lines quickly without opening an editor like Nano.

    Command:
    cat > myfile.txt
Type your text: Type your lines. You can hit Enter to go to a new line as many times as you like.

Save and Exit: When you are done, press Ctrl + D. This tells the terminal "I am done typing" and saves the file.

How to check if it worked

To verify that your file was created and the text is inside, use the cat command to read it:

    cat myfile.txt

***Method 1 (Nano)***

Since Nano is a keyboard-based editor, you cannot use your mouse to move the cursor or click buttons. You must use keyboard shortcuts.

***Understanding the Notation***

When you look at the bottom of the Nano screen, you will see shortcuts listed like ^X or ^O.

^ (Caret symbol): This stands for the Ctrl key on your keyboard.

Example: ^X means you should press and hold Ctrl, then press X.

***Nano Command Cheat Sheet***

Here are the most helpful commands you will use while inside the editor:

Save File
    
    Ctrl + O
    
    """Write Out"". Saves your changes to the disk. You will need to press Enter to confirm the filename."

Exit Nano

    Ctrl + X

    "Closes the editor. If you haven't saved, it will ask Save modified buffer? (Press Y for Yes, N for No)."

Search
    
    Ctrl + W

    """Where Is"". Opens a search prompt. Type a word and hit Enter to find it."

Find Next

    Alt + W

    "After searching once, use this to find the next occurrence of that word."

Cut Line

    Ctrl + K

    Deletes the entire line your cursor is currently on (like a cut command).

Paste Line

    Ctrl + U

    """Uncut"". Pastes the line you just deleted (used to move text around)."

Go to Line

    Ctrl + /_

    Press Ctrl and _ (underscore) or Shift + - to jump to a specific line number.

Get Help

    Ctrl + G

    Opens the help manual within Nano if you forget a command.

***Essential Editing Tips***

#How to Copy/Paste blocks of text

Nano doesn't handle "highlighting" text with a mouse like Word does.

Move your cursor to the start of the text.

Press Ctrl + 6 (or Alt + A) to set a "Mark".

Move the cursor to the end of the text (it will highlight).

Press Alt + 6 to Copy (or Ctrl + K to Cut).

Move to where you want it and press Ctrl + U to Paste.

#How to replace text

If you want to find a word and replace it with another:

Press Ctrl + \ (Backslash).

Type the word to find and press Enter.

Type the replacement word and press Enter.

Press A to replace All occurrences, or Y to replace just the one.

***Common Terminal Flags for Nano***

These are commands you type in the terminal before opening Nano to make your life easier.

Open as Administrator (Important): If you are editing a system file (like a config file), you won't be allowed to save it unless you use sudo.


    sudo nano /etc/hosts
Open with Line Numbers: Helpful for coding or debugging.


    nano -l myfile.txt
Open at a specific line: If an error log tells you there is an error on line 50, you can open the file directly at that line.


    nano +50 myfile.txt
