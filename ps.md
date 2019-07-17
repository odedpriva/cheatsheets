# ps

- `ps e` is interesting for showing environment variables
- `ps aux | awk '$8 !~ /S/'` - find processes in state D, mostly, but unexpected R and Z 

- `ps auxwww` - long output
- `ps -o pid=,rss=,cmd= $(pgrep python)`

kill <signal> $(ps -fe | grep <pattern> | awk '{print $2}')

sorting process
---

- `ps -ef --sort=user,cmd`
- `ps -ef --sort=-start_time | head`