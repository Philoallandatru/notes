- Re-implement one of the systems described in the papers discussed in 6.824.
- Build a high-performance Raft implementation, changing the design as needed.
- Build a distributed, decentralized, fault-tolerant Reddit.
- Build a system for making Node.js applications fault-tolerant, perhaps using some form of replicated execution.
- Add cross-shard atomic transactions to Lab 4, using two-phase commit and/or snapshots.
- Build a data-flow processing system in the style of Google FlumeJava or Spark or Naiad.
- Build a system with asynchronous replication (like Dynamo or Ficus or Bayou). Perhaps add stronger consistency (as in COPS or Walter or Lynx).
- Build a file synchronizer (like [Unison](http://www.cis.upenn.edu/~bcpierce/unison/) or [Tra](http://swtch.com/tra/)).
- Build a coherent caching system for use by web sites (a bit like memcached), perhaps along the lines of [TxCache](http://drkp.net/papers/txcache-osdi10.pdf).
- Build a distributed cooperative web cache, perhaps along the lines of [Firecoral](https://www.usenix.org/legacy/events/iptps09/tech/full_papers/terrace/terrace_html/) or [Maygh](http://www.ccs.neu.edu/home/amislove/publications/Maygh-EuroSys.pdf).
- Build a collaborative editor like EtherPad, using eventually-consistent or CRDT primitives.
- Use a block-chain to build something other than a crypto-currency.
- Build a fault-tolerant and/or sharded file service.
- Build a [distributed shared memory](http://www.cdf.toronto.edu/~csc469h/fall/handouts/nitzberg91.pdf) (DSM) system, to make it possible to run existing parallel code intended for a single multi-core machine, but on a cluster of machines.
- Build a distributed block store in the style of Amazon EBS or FAB. Maybe you can get standard operating systems to talk to you network virtual disk using iSCSI or Linux's NBD (network block device).
- Build a geo-replicated storage system, like Dynamo or COPS, perhaps providing something useful and/or efficient in the the way of transactions or consistency.
- Use modern high-speed NIC features (e.g. RDMA or DPDK) to build a high-speed service, perhaps with replication or transactions.
- Use modern fast non-volatile storage (e.g. Intel Optane) to simplify the design of a fault-tolerant system.
- Build a fault-tolerance framework that's easier than Raft to layer service code on top of.
- Figure how to say something useful about whether applications really need strictly consistent storage, or what the cost in application complexity is of having to use storage with weak consistency.
- Build a data-processing system that is good at both big data (like MapReduce and Spark) and on-line processing (like a key/value store or SQL database).