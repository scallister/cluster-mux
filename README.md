# cluster-mux
Helper script for sshing and controlling several hosts while in a tmux session. This is similar to cluster ssh. Hostnames can be piped to cluster-mux or can be listed as arguments. Cluster-mux will then open the new hosts in a new window with each pane representing one host with an ssh connection.

## Examples
A list of hosts can be piped to cluster-mux. In this case all_hosts is a command that returns a list of hosts delineated by newlines from Salt. I then grep for the hosts I'm interested in and pipe those to cluster-mux.
```
all_hosts | grep -i deploy  | grep -iv new  |grep -iv ops | cluster-mux
```
