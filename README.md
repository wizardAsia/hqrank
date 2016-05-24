﻿# hqrank
支持并发的实时排行、排行榜工具-java

hqrank是一个实施排行工具。

目前hqrank的实现包括如下几点：

1、全缓存
所有的排行数据存储在内存中。所以，hqrank是作为一个排行工具，而不是数据存储工具而存在

2、基于id:value
对数据的存取可以通过id-value进行，可通过id获取对应排名，也可以通过排名获取对应id。（value也会在此给出）

3、支持多字段排行
比如先按等级排行，在此基础上再按经验排行，进而得出的排行列表。理论上支持任意多的字段数

4、支持并发
支持多个线程同时对排行进行操作

5、实时排行
排行操作是实时进行的，但需要说明一点：对于访问时间相差很少的两个访问，尤其是不同线程，可能不会严格满足先入先排，但这种相差时间是在毫秒级的（这和线程时间片以及系统提供加锁顺序相关）


工具还在开发过程中，还没有经过大量测试，如果有对此有兴趣的Coder，欢迎一起讨论和开发

#  使用 how to use

hqrank/code/Rank/是一个java项目，jdk版本为：1.7.0_45
1、将该项目导入eclipse中
2、在包org/hq/rank/service/中有IRankService.java，里面有详细的注释
