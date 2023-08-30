command (if host excist in config file) -> `ssh host`
otherwise -> `ssh user@host`
use `-o` for options like HostKeyAlgorithms or IdentityFile

example -> `ssh me@hpc -o HostKeyAlgorithms=+ssh-rsa`

## config file
address: ~/.ssh/config

HOST [NAME] 
	User [USER]
	HostName [DOMAIN or IP address]
	IdentityFile [path]
	HostKeyAlgorithm=[key,...]

HostKeyAlgorithms are like ssh-rsa, ssh-dss or ed25519.

# ssh keygen
command: `ssh-keygen -t TYPE -C COMMENT

- TYPE: type of encryption key, for examples: rsa, ed25519 (more `man ssh-keygen`)
- also you can put `-b 4096` for larger size key (default key size is 2048 for RSA)
- COMMENT: extra comment for example you can put YOUREMAIL to access github from ssh

# ssh-add
command: `ssh-add PRIVATEKEY`

this command adds a private key from location PRIVATEKEY to your identification list
