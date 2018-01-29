# ssh
* Secure Shell is a protocol used to securely log onto remote systems.
* It can be used for logging or executing commands on a remote server.

1. Connect to a remote server:
* ssh username@remote_host

2. Connect to a remote server with a specific identity (private key):
* ssh -i path/to/key_file username@remote_host

3. Connect to a remote server using a specific port:
* ssh username@remote_host -p 2222

4. Run a command on a remote server:
* ssh remote_host command -with -flags

5. SSH tunneling: Dynamic port forwarding (SOCKS proxy on localhost:9999):
* ssh -D 9999 -C username@remote_host

6. SSH tunneling: Forward a specific port (localhost:9999 to slashdot.org:80):
* ssh -f -L 8080:localhost:8080 utility.staging.luminateops.com -N

## links
- https://explainshell.com/