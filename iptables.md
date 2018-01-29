# iptables

1. show all tables
* sudo iptables -L

2. show all tables verbose
* sudo iptables -nvL

3. basic rules
* iptables -A INPUT -i lo -j ACCEPT
* iptables -A INPUT -m conntrack -ctstate ESTABLISHED,RELATED -j ACCEPT
* iptables -A INPUT -p tcp --dport 22 -j ACCEPT

4. export tables 
* sudo iptables-save > table

5. import table
* sudo iptables-restore < table