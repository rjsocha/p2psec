# p2psec

Create p2p ipsec (full mesh) network

PSK only

for PoC 


usage:

define PEERS in /etc/default/p2psec

in the format:
  ip1:internal_ip1 ip2:internal_ip2 ipN:internal_ipN
  
  where ip1,ip2 - peers ip addresses
  internal_ip1,internal_ip - tunnels endpoints (binded to lo)
  
  you need to setup the same config on all peers (nodes)
  
  set AUTH_KEY and ENC_KEY (sha256 and twofish by default)
  
  and run:
  
  systemctl restart p2psec
  
  tested on: debian and ubuntu only (10/20.04)
  
  
