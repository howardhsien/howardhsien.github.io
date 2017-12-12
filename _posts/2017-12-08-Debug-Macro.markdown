---
layout: post
title: DEBUG Macro
---

### DEBUG trace
``` C
#define __FILENAME__ (strrchr(__FILE__, '/') ? (strrchr(__FILE__, '/') + 1):__FILE__)
#define sys_trace(fmt, args...)    do { if(DEBUG_MODE) printf("%s:%d:%s(): " fmt, __FILENAME__, __LINE__, \
			__FUNCTION__, ##args); }while(0)
```
sample output :
```
upg_commsrv.c:234:commsrv_getdata(): (num_read != read_cnt) num_read=496, read_cnt=21467
```
