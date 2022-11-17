# Translation

### (my) Questions

#### Why we need virtual memory?(the translation from PA to VA)

It will be easier to implementation protection with translation. Because task A cannot even gain access to data of task B

Give the process an illusion that it owns the entire memory space.





VA = P # + Offset

Question: Why we need this? This doesn't change the size of the memory.

*I think it is useful to provide safety(the access field) and the base and bound register, it is safe, I know

## Paged Memory

重点：这是一些定长的块，这意味着这些块易于被分配；但是如果不用的就浪费。对比segmented memory，不用的地方可以通过移动用的地方来使得物理内存变得紧致的。

好像上面所讲的问题就是内部碎片？

另一点，无论页表大还是页大都会浪费空间。

话说为什么页表大也会浪费空间？好像是因为有很多页都没有被用到吗？

It seems that you can adjust the segment but you can not do the same things with  pages. Since it is fixed size, and it should be much smaller than segment.

Example: 

## Multi-level Translation

这个可以用：在各式各样的情况下，怎么能最有效率地通过key找到value的方式来类比吗?



# Brief of Cache 

You want to know the value of a given address(in memory, there are (address, value) pairs). So you consult the cache.

## What's a cache?



读的延迟 = 中的概率 乘 中的延迟 加 不中的概率 乘 不中的延迟

话说，中的延迟是什么？

写的操作（也就是）会被缓冲起来？堆很多写操作然后一起告诉cache吗？但好像是……只要buffer中还有空间，数据就会被马上写入。

如果key not in map,     

### Memory Hierachy 内存分级

重要的是知道这十个等级的速度的跨度是指数级的                                                               

​	

# 问题

### Why the size of the page table is proportional to the size of the virtual table size instead of the physical memory space?





