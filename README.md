# vpn-server

OpenVPN is a full-featured SSL VPN (virtual private network). It implements OSI layer 2 or 3 secure network extension using the SSL/TLS protocol. It is an open source software and distributed under the GNU GPL. A VPN allows you to connect securely to an insecure public network such as wifi network at the airport or hotel. VPN is also required to access your corporate or enterprise or home server resources. You can bypass geo-blocked site and increase your privacy or safety online. This tutorial provides step-by-step instructions for configuring an OpenVPN “road warrior” server on Ubuntu Linux 18.04/20.04 LTS (20.10) version including ufw/iptables firewall configuration. The steps are as follows:

Referece :
- [howto-setup-openvpn-server-on-ubuntu-linux](https://www.cyberciti.biz/faq/howto-setup-openvpn-server-on-ubuntu-linux-14-04-or-16-04-lts/)
- [Repo Nyr](https://github.com/Nyr/openvpn-install)


1. [Find and note down your public IP address](#Find-and-note-down-your-public-IP-address)
2. Download openvpn-install.sh script
3. Run openvpn-install.sh to install OpenVPN server
4. Connect an OpenVPN using client


### Find and note down your public IP address:

```sh
$ dig -4 TXT +short o-o.myaddr.l.google.com @ns1.google.com
```

###  Find and note down your public IP address:

```sh
$ wget https://git.io/vpn -O openvpn-install.sh
```

We can verify script using a text editor such as nano command or vim command:
```sh
$ nano openvpn-install.sh
```
### Run openvpn-install.sh to install OpenVPN server:

Type the following command:
```sh
$ sudo chmod +x openvpn-install.sh
```

```sh
$ sudo bash openvpn-install.sh
```

Make sure you provide needed information:
```txt
Welcome to this OpenVPN road warrior installer!

This server is behind NAT. What is the public IPv4 address or hostname?
Public IPv4 address / hostname [....]:

Which protocol should OpenVPN use?
   1) UDP (recommended)
   2) TCP
Protocol [1]: 

What port should OpenVPN listen to?
Port [1194]:

Select a DNS server for the clients:
   1) Current system resolvers
   2) Google
   3) 1.1.1.1
   4) OpenDNS
   5) Quad9
   6) AdGuard
DNS server [1]:

Enter a name for the first client:
Name [client]: 
```

### Connect an OpenVPN using client: 
Download from [openvpn](https://openvpn.net/client-connect-vpn-for-windows/) the proper client

