# Distributed-Cache

This is a concurrent and HTTP-based distributed cache for golang, based on [groupcache](https://geektutu.com/post/geecache.html#:~:text=%E5%9F%BA%E6%9C%AC%E4%B8%8A%E6%A8%A1%E4%BB%BF%E4%BA%86-,groupcache,-%E7%9A%84%E5%AE%9E%E7%8E%B0%EF%BC%8C%E4%B8%BA%E4%BA%86)

Utilized LRU for cache replacement policy

Applied Consistent Hashing for distributed nodes. Achieved peers selection, peer registration and HTTP client.

Designed Single Flight to prevent Cache Breakdown.

Utilized Protobuf for higher efficient in transition and better expandability.

Test:

```
$ sudo ./run.sh
2023/07/01 21:54:24 [Server http://localhost:8003] Pick peer http://localhost:8001
2020/07/01 21:54:24 [Server http://localhost:8001] GET /_distributedcache/scores/Tom
2020/07/01 21:54:24 [SlowDB] search key Tom
630630630
```

If you want to run this program, please install go 1.13 and protobuf under linux.

Reference: https://geektutu.com/post/geecache.html
