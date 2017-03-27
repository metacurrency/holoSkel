# holoSkel
skeleton template for building a holochain app

#### Testing your holochains
##### To test holochain
1. place a script for each role in the directory: Scripts/cluster/hc/
    * ***WARNING YOU MUST*** HAVE `#!/bin/sh` as the first line of the script
    * Your seeded holochain is at /chain.seeded/devchain
    * example script that loads and serves the holochain. For example:
        ```bash
        #!/bin/sh
        hc init $HOSTNAME
        hc join /chain.seeded/devchain myHCInstance
        hc serve myHCInstance
        ```
    * Scripts should be named following this convention:
    
      1.someFileName.indicatingRole1
      
      2.someFileName.indicatingRole2
      
      3.someFileName.indicatingRole3
      ...
      
    * Should you need it, the shared filesystem is writable (/chain.seeded/devchain)
      
2. when ready, run `Scripts/tests/test.HC`
