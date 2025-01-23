## Access Methods
* Console - Out-of-band access management
* SSH - In-band remote management (SECURE)
* Telnet - In-band remote management (PLAINTEXT)

## Switch Configuration
* `enable` - This enables privileged mode
* `configure terminal` - This enters the global configuration mode
* `hostname ___` - Specify the name of the switch
* `enable secret ___` Specify encrypted password for privileged exec mode
* `banner motd #___#` Configure the banner ('#' is the delimiter. Start and End)
* `line console 0` - (Line Configuration Mode) Used to configure console, SSH, Telnet, or AUX Access
```
line console 0
password cisco
login
line vty 0 15 # VTY - Virtual Terminal Interface
```
