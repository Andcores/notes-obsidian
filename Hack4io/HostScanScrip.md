![[Pasted image 20240930191649.png]]



```
#!/bin/bash
for i in $(seq 1 254);do
	timeout 1 bash -c "ping -c 1 192.168.1.$i &>/dev/null" && echo "[+] 192.168.1.$i - ACTIVE" &
done;wait
```

