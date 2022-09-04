# Concordium snapshot
Setting up a fully synchronized node in a couple of clicks

First of all, you need to install the node, following the official guide, run the node once, see it on the dashboard and then stop it. Next, go to the database directory. The location of the database directory differs depending on your system:
```
Linux systems: /var/lib/concordium-9dd9ca4d19e9393877d2c44b70f89acbfc0883c2243e5eeaecc0d1cd0503f478/data/database-v4
MacOs: /Library/Application Support/Concordium Node/Mainnet/Data/database-v4
Windows: C:\ProgramData\Concordium\Node Runner\mainnet\data\database-v4
```

Delete treestate-0 and blockstate-0.dat. Download the archive and unpack its contents into this directory. After unpacking into the database-v4 directory, you should have a consistent set of treestate- directories and blockstate- files.

If you are using linux systems, you will also need to set special permissions for the concordium-mainnet-node user to access the contents of the database-v4 directory using the command:
`sudo chown 65396:65396 database-v4/ -R`

[Download archive](http://pablo-snapshot.ddns.net)
