# rados_t
```C
typedef void *rados_t;
```
其实际定义：
```C
reinterpret_cast<rados_t>(new librados::RadosClient(cct));
```
## rados_t实例的创建和销毁
```C
int rados_create(rados_t *cluster, const char * const id);
int rados_create2(rados_t *pcluster, const char *const clustername, const char * const name, uint64_t flags);
int rados_create_with_context(rados_t *cluster, rados_config_t cct);

void rados_shutdown(rados_t cluster);
```

```C
int rados_create(rados_t *cluster, const char * const id);
```

```C
int rados_create_with_context(rados_t *cluster, rados_config_t cct);
```
用于不同的cluster实例中共享配置，See：`rados_cct`函数

```C
int rados_ping_monitor(rados_t cluster, const char *mon_id, char **outstr, size_t *outstrlen);
```
Ping the monitor with ID mon_id, storing the resulting reply in `buf` (if specified) with a maximum size of len. The result buffer is allocated on the heap; the caller is expected to release that memory with rados_buffer_free().  The buffer and length pointers can be NULL, in which case they are not filled in.
