# elasticutils

## elasticless

```
# just run default query * against localhost:9200 and syslog-YYYY.MM.DD daily index
# and page results
elasticless
2018-11-06T11:19:04Z node42.example.com xinetd EXIT: foo status=0 pid=19627 duration=0(sec)
2018-11-06T11:19:04Z node42.example.com interface-em4/if_octets/rx/avg/30 null
2018-11-06T11:19:04Z node41.example.com systemd Started kubelet: The Kubernetes Node Agent.
Press 'q|Q|x|X' to exit or any key to continue
```

```
# run custom query against custom index prefix
# and send to file
EL_INDEX_PREFIX=samplerr- elasticless 'host:node42 AND service:sshd' > out.csv
```

```
# run default query and send to file as JSON
EL_RAW_OUTPUT=1 elasticless > out.json
```

