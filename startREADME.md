# atposone
check -> curl 127.0.0.1:9101/metrics 2> /dev/null | grep aptos_state_sync_version | grep type
port? -> nc -zvv 158.247.223.130 6180, 8080, 9101
inbound,outbound -> curl 127.0.0.1:9101/metrics 2> /dev/null | grep "9ae46560"
