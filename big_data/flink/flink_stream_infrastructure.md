流数据：

* 永不停止、无尽的数据流
* 实时、低延迟的数据分析

传统的数据分析是采用中心化的数据库系统，存储事务性数据，使用SQL（或NoSQL）对历史数据进行分析：

* 数据不是经常更新的
* 数据分析所需的工作流程复杂而且缓慢
* 由于中心化数据存储，大量的应用程序访问数据库压力极大，导致响应缓慢；而采用缓存（Memcache之类）则难以保证数据的一致性
* 为了保证数据一致性，分布式数据库需要复杂的同步和异常处理机制，代价极大

**流处理架构降低了对大规模分布式数据一致性的要求，只需要维持本地数据的一致性。**

在流数据架构中，没有一个数据库来集中存储全局状态数据，而是共享永不停止的流数据，记录了业务数据的历史。在流数据架构中，每个应用程序都有自己的数据，并采用本地数据库或者分布式文件进行存储。



# 参考

* 「Flink基础教程」