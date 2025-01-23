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
#### Configuring a Password
```
line console 0    # Protects Out-of-Band connections (Physical)
password cisco    # Sets the password to "cisco"
login             # Enables the password to prompt on login
line vty 0 15     # Protects In-Band connections (Not Physical)
password cisco    # Sets the password to "cisco"
login             # Enables the password to prompt on login
```
