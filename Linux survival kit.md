# Linux survival kit
## Linux release
Kernel version:         uname -r 
Distribution versions:  lsb_release -a
Package version:        dpkg    -l openssl
                        rpm -qa | grep openssl

## PGP Web of trust
keyserver: http://pool.sks-keyservers.net/

pgpk -c verifys all signatures and shows the values for every key in the keyring
pgp -kc verifys all signatures and should be called prior using pgp -km
pgp -km shows the values