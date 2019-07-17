# dig - DNS Lookup utility

1. Lookup the IP(s) associated with a hostname (A records):
* dig +short hostname.com

2. Lookup the mail server associated with a given domain name (MX record):
* dig +short hostname.com MX

3. Specify an alternate DNS server to query (8.8.8.8 is google's public DNS):
* dig @8.8.8.8 hostname.com

4. Perform a reverse DNS lookup on an IP address (PTR record):
* dig -x 8.8.8.8

5. Find authoritative name servers for the zone and display SOA records:
* dig +nssearch hostname.com

6. get current ip 
`dig o-o.myaddr.l.google.com @ns1.google.com txt +short`

## install

* sudo apt-get install dnsutils

