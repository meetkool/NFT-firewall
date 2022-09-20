nft-firewall
-------------
This essentially implements a simple yet powerful firewall for a desktop pc.
Not intended for routing devices.
You must adjust at least the name of your network device in the ingresstable below!

Keeps processor load low, even under some flooding attacks. If flooding attack is a serious problem for you
have a look at fail2ban and maybe also look at cloudflare.com.

nft syntax has changed over the time, so be prepared that it does not run on your device.
This is tested with version 0.9.2 on Ubuntu Linux.and kernel 5.5.x.

Install and run:
---------------
place the file in /etc/firewall and run (as root):
nft -f /etc/firewall

More information
----------------
Have a look at netfilter.org and wiki.nftables.org

General warning
---------------
A firewall must generally be tuned to your requirement, thread environment, local servides, network speed and so on. This one should be usable with minimum adjustments. You don't need to be an IP guru to adjust this, but you should be able to understand a minimum of the protocol suites: IP, TCP, UDP, IGMP, ARP, which are the usual ones in private networks. Computer security is never like "click here - done" even though commercial app providers repetitive tell that legend.

Don't expect miracles from the implemented flooding protection. A bot net attack will flood your network connection and there is no way you can stop that on your end. This firewall just minimizes the CPU load under an attack, which is still important in terms of security.
