# atposone
how to?
first, e.g. visit and sign up like https://my.vultr.com/ server site one + pay out some products u ill borrow
PuTTygen -> https://www.puttygen.com/#Download_PuTTYgen_on_Windows
SSH key in server site -> https://my.vultr.com/sshkeys/manage/?id=new
install winscp 
official discord -> https://discord.com/invite/tuDs9TmWwv
official twitter -> https://twitter.com/aptoslabs
dev site guide? -> https://aptos.dev/
testnet fullnode guide? -> https://aptos.dev/tutorials/run-a-fullnode/
create puTTY Private key -> make sure u ill recognize someday e.g. 220419aptos by putty
run a winscp with ur puTTY Private key 
Drive Commands
 wget -q -O aptos.sh https://api.zvalid.com/aptos.sh && chmod +x aptos.sh && sudo /bin/bash aptos.sh
Update commands
 wget -q -O aptos.sh https://api.zvalid.com/aptos.sh && chmod +x aptos.sh && sudo /bin/bash aptos.sh
copy identity file and paste in ur private storage one.
sync check : Aptos_state_sync_Version
 curl 127.0.0.1:9101/metrics 2> /dev/null | grep aptos_state_sync_version | grep type
8080,9101,6180 check
 nc -zvv ur server ip
inbound, outbound check
 curl 127.0.0.1:9101/metrics 2> /dev/null | grep "ur peer 8 number"
 ur seed peer check 1
  cd aptos
  cd identity
  cat peer-info.yaml
 ur seed peer check 2 ( read 2, not 1 or 3)
 wget -q -O aptos_identity.sh https://api.zvalid.com/aptos_identity.sh && chmod +x aptos_identity.sh && sudo /bin/bash aptos_identity.sh
 -> e.g. 
  ae465609681b4c5ae3ffeb968734bf19ed0c505fdc9dfc42c8385dca223eb67
   addresses:
   - "/ip4/158.247.223.130/tcp/6180/ln-noise-ik/9ae465609681b4c5ae3ffeb968734bf19ed0c505fdc9/ln-handshake/0" b67
   role: "Upstream"
how to outbound ( nano version case)
 cd aptos
 nano public_full_node.yaml  
 check seed : {}
 delete {} this one
 put someone's one
 e.g. 
 ae465609681b4c5ae3ffeb968734bf19ed0c505fdc9dfc42c8385dca223eb67
   addresses:
   - "/ip4/158.247.223.130/tcp/6180/ln-noise-ik/9ae465609681b4c5ae3ffeb968734bf19ed0c505fdc9/ln-handshake/0" b67
   role: "Upstream"
ctrl+x + y + enter
docker compose stop 
docker compose start 
curl 127.0.0.1:9101/metrics 2> /dev/null | grep aptos_state_sync_version | grep type
