# holoSkel
skeleton template for building a holochain app

#### Testing your holochains
##### To test holochain
1. place a script for each role in the directory: Scripts/cluster/hc/
2. run Scripts/tests/test.HC

Each script has access to a seeded holochain, located at /chain.seeded/devchain
```bash
#!/bin/sh
hc init $HOSTNAME
hc join /chain.seeded/devchain myHCInstance
hc serve myHCInstance
```
#WARNING YOU MUST HAVE #!/bin/sh as the first line of the script
