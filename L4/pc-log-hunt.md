```bash
grep FLAG ~/Downloads/server.log | sed "s/\[.*: //" | sort --unique | paste -d" " - - - - | awk '{print $2$4$3$1}'
```