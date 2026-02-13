Вот решение:
awk '$1!="" {ip=$1; size=$10; result[ip]+=size} END {for(ip in result) print result[ip] " size for " ip}' access.log

awk '$1!="" {ip=$1; size=$10; result[ip]+=size} END {for(ip in result) print result[ip] " size for " ip}' access.log > result.log