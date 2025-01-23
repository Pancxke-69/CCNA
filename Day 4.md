## Access Methods
* Console - Out-of-band access management
* SSH - In-band remote management (SECURE)
* Telnet - In-band remote management (PLAINTEXT)

## Switch Configuration
* `enable` - This enables privileged mode
* `configure terminal` - This enters the global configuration mode
* `hostname ___` - Specify the name of the switch
* `enable secret ___` Specify encrypted password for privileged exec mode
* `enable password ___` Specify plaintext password for privileged exec mode
* `banner motd #___#` Configure the banner ('#' is the delimiter. Start and End)
* `line console 0` - (Line Configuration Mode) Used to configure console, SSH, Telnet, or AUX Access
* `end OR CTRL+Z` - Takes you all the way back to privileged mode
* `exit` - Takes you back one section
* `logging synchronous` - Stops Pop-Up Messages
* `exec-timout <0-35791>` - Changes the timeout in minutes (0 will disable completely)
#### Configuring a Password
```
enable
configure terminal
line console 0    # Protects Out-of-Band connections (Physical)
password cisco    # Sets the password to "cisco"
login             # Enables the password to prompt on login
line vty 0 15     # Protects In-Band connections (Not Physical)
password cisco    # Sets the password to "cisco"
login             # Enables the password to prompt on login
exit
enable secret class    # Sets password for exec to "class"
```
## Shortcuts
* `Tab`	- Completes a partial command name entry.
* `Backspace` - Erases the character to the left of the cursor.
* `Ctrl+D`	- Erase s the character at the cursor.
* `Ctrl+K` - Erases all characters from the cursor to the end of the command line.
* `Esc D`	- Erases all characters from the cursor to the end of the word.
* `Ctrl+U or Ctrl+X` - Erases all characters from the cursor back to the beginning of the command line.
* `Ctrl+W` - Erases the word to the left of the cursor.
* `Ctrl+A` - Moves the cursor to the beginning of the line.
* `Left Arrow or Ctrl+B` - Moves the cursor one character to the left.
* `Esc B`	- Moves the cursor back one word to the left.
* `Esc F`	- Moves the cursor forward one word to the right.
* `Right Arrow or Ctrl+F` -	Moves the cursor one character to the right.
* `Ctrl+E` - Moves the cursor to the end of command line.
* `Up` - Arrowor Ctrl+P	Recalls the previous command in the history buffer, beginning with the most recent command.
* `Down` - Arrowor Ctrl+N	Goes to the next line in the the history buffer.
* `Ctrl+R or Ctrl+I or Ctrl+L` -	Redisplays the system prompt and command line after a console message is received.
