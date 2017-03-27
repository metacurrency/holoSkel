# holoSkel
skeleton template for building a holochain app

#### Testing your holochains
##### To test holochain
1. place a script for each role in the directory: Scripts/cluster/hc/
  # WARNING YOU MUST HAVE #!/bin/sh as the first line of the script
  * Your seeded holochain is at /chain.seeded/devchain
  * example script that loads and serves the holochain
  ```bash
  #!/bin/sh
  hc init $HOSTNAME
  hc join /chain.seeded/devchain myHCInstance
  hc serve myHCInstance
  ```
2. run Scripts/tests/test.HC
