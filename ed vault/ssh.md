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