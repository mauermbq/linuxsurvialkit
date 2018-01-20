# Linux

## Linux OS and env info

Kernel version:         uname -r
Distribution versions:  lsb_release -a
Package version:        dpkg    -l openssl
                        rpm -qa | grep openssl

dmesg -k: print kernel messages
uptime: uptime since last reboot
write: send a message to another user
printenv: print all or part of environment
which \<commanbd\>:       locate a command
free:     memory
df -m:    disk usage and free space in megabites
last: show last logins
who: logged in users
id: UID including group ids and names
w - Show who is logged on and what they are doing

## file handling (beside ls, mkdir, rm, cp)

head:       shows first lines of a file
tail -f:    shows lst lines of a file and output appended data as the file grows
touch:      change file time stamp or create empty file
ln -s /path/to/file /path/to/symlink
cat:        concatenate files and print on the standard output
du:         estimate file space usage
split:      split a file into pieces
cmp:        compare files
chmod:      `[ugoa]*([-+=]([rwxXst]*|[ugo]))+'

## APT

apt-cache policy \<package\>: available package versions or
apt list -a <package>
apt search <keyword>:       search for package
apt autoremove:             remove unreferenced packages

## PGP Web of trust

keyserver: http://pool.sks-keyservers.net/

pgpk -c verifys all signatures and shows the values for every key in the keyring
pgp -kc verifys all signatures and should be called prior using pgp -km
pgp -km shows the values

## Network

netstat -A inet: internet connections
route - show / manipulate the IP routing table

## ssh

ssh-keygen -t rsa -b 4096: generate key pair with rsa algorithm and keysize 4096
ssh-copy-id -i: copy key file to authorized keys at the server
see /etc/ssh/sshd_config on server and /etc/ssh/config on client


Any organization that doesn't control they SSH key based access is probably
in breach of EU GDPR, Sarbanes-Oxley, PCI DSS, HIPAA, NIST SP 800-53 
Guidance: https://www.ssh.com/compliance/nist-7966/