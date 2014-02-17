bash deploy script with rsync and git
=====================================

bash script for retrieving code from git and pushing to a server with rsync

#### Requirements
- Bash 4
- Git
- rsync


#### Install
```
curl -sS https://raw.github.com/eigan/deploy/master/deploy > /usr/local/bin/deploy
chmod 755 /usr/local/bin/deploy
```

#### Usage
```
Usage deploy <server> [OPTIONS]
Usage deploy init (creates the deploy.conf)

Option        Meaning
init          Creates the deploy.conf file
-b <branch>	  The git branch
-c <file>	  Path to config file (default: deploy.conf)
-h		      This help screen
-s <server>	  The server (defined in deploy.conf)
-t		      Run in testmode, will stop before we start executing
-v		      Display extra info about whats going on
```

Standard usage would be to just 'deploy prod'. Edit deploy.conf and add commands to run on the repo before syncing.
