This guide is not official, licensed or owned by the Concordium organization.

# Concordium snapshot
Setting up a fully synchronized node in a couple of clicks. 
The full database archive is updated once a week on Sundays. The partial database repair archive is updated every day and has the words latest_blocks in the title.

First of all, you need to install the node, following the official guide, run the node once, see it on the dashboard and then stop it.
Next, go to the database directory. The location of the database directory differs depending on your system:
```
Linux systems: /var/lib/concordium-9dd9ca4d19e9393877d2c44b70f89acbfc0883c2243e5eeaecc0d1cd0503f478/data/database-v4
MacOs: /Library/Application Support/Concordium Node/Mainnet/Data/database-v4
Windows: C:\ProgramData\Concordium\Node Runner\mainnet\data\database-v4

Docker: You choose the directory yourself, see your yaml config to view the database directory
```

You can clean up any files in this directory, e.g. treestate-x and blockstate-x.dat. [Download archive](http://pablo-snapshot.ddns.net) and unpack its contents into database-v4 directory. After unpacking, you should have a serial set of treestate- directories and blockstate- files.


If you are using linux systems (not related to docker), you may also need to set special permissions for the concordium-mainnet-node user to access the contents of the database-v4 directory using the command:
`sudo chown 65396:65396 /var/lib/concordium-9dd9ca4d19e9393877d2c44b70f89acbfc0883c2243e5eeaecc0d1cd0503f478/data/database-v4 -R`
Do this if there is a problem accessing unpacked files
