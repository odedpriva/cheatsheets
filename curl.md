# curl 

## options
curl --show-error --user-agent Homebrew/1.5.8 (Macintosh; Intel Mac OS X 10.13.4) curl/7.54.0 --fail --location --remote-time --continue-at - --output /Users/odedpriva/tmp/${random}.incomplete 

## unix socket

curl --unix-socket /var/run/docker.sock http://localhost/info | jq