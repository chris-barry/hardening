# SSH

Sample hardened configuration file.

```
Protocol 2

PermitRootLogin no
AllowTcpForwarding no
X11Forwarding no

# Prevent you from logging in without a public key.
IgnoreRhosts yes
HostbasedAuthentication no
RhostsRSAAuthentication no
```
