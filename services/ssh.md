# SSH

Sample hardened configuration file.

```
Protocol 2

# Prevent most from logging in.
PermitRootLogin no
AllowUsers user1,user2,...usern

# We don't want X11 (not always needed).
AllowTcpForwarding no
X11Forwarding no

# Prevent you from logging in without a public key.
IgnoreRhosts yes
HostbasedAuthentication no
RhostsRSAAuthentication no
```
