执行命令rbd create rbd_write --size 1024 --pool data或者rbd create rbd_write --size 1024 -p data创建rbd块设备
* rbd_write代表所创建rbd块设备的名字
* --size后接rbd块设备的大小，单位MB
* --pool后接该rbd块设备所在存储池名称

执行命令rbd ls -p data查看存储池中已创建的块设备

$> rbd disk-usage
$> rbd du
Show disk usage stats for pool, image or snapshot
