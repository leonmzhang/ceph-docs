ceph -s
```
$> ceph -s
    cluster c96f2627-3243-444e-9d96-01444766e8f0
     health HEALTH_OK
     monmap e1: 1 mons at {ceph02=172.31.65.3:6789/0}
            election epoch 3, quorum 0 ceph02
     osdmap e9: 1 osds: 1 up, 1 in
            flags sortbitwise,require_jewel_osds
      pgmap v969: 64 pgs, 1 pools, 0 bytes data, 0 objects
            1033 MB used, 101315 MB / 102348 MB avail
                  64 active+clean
```

# cluster
# health
health 有几种状态
```C
// src/include/types.h
enum health_status_t {
  HEALTH_ERR = 0,
  HEALTH_WARN = 1,
  HEALTH_OK = 2,
};
```

