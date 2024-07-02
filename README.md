## 查看 cluster-info, -c → cluster mode 下進行指令

```yaml
redis-cli -c -h <ip> -p <port> -a <password> cluster info
```

## 修復 cluster, 重新分配 slot

```yaml
redis-cli --cluster fix <ip>:<port> -a <password>
```

## 了解 master-slave 節點間對應關係

```yaml
redis-cli --cluster check <ip>:<port> -a <password>
```

## set / get value

```yaml
set k1 <value>.  get k1
```

## 算出的 slot 數值

```yaml
CLUSTER KEYSLOT <key>
```

## 將新的 master node 加入 cluster

```yaml
redis-cli --cluster add-node  <ip>:<port> <ip>:<port> -a <password>
```

## 重新分配 slot

```yaml
redis-cli --cluster reshard <ip>:<port> -a redisCluster
```

## 將 slave 掛載到 master node 上面

```yaml
redis-cli --cluster add-node <slave-ip>:<port> <master-ip>:<port>  --cluster-slave --cluster-master-id <id> -a <password>
```
