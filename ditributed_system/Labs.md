# 6.834 Labs

## Lab 1: MapReduce

### 	Info



网页的信息：

- 实现`coordinator`和`worker`
- 一个`coordinator`进程，多个`worker`进程
- `worker`通过RPC和`coordinater`沟通，要求`coordinator`给他一个任务。从一个或者多个文件中读入任务的输入，执行任务，然后把任务的输出写到一个或者多个文件中。
- `coordinator`：如果一个工人在一定时间（例如10秒）内没有完成任务，那就把同样的任务分给其他的工人。

在开始这个项目的时候，需要思考的是：

需要哪些抽象？哪些抽象是已经提供的，还需要设计哪些抽象？

每个抽象的职责是什么？要做什么事？

协调者（coordinator）：

工人（worker）：

### 	Existing Code

`mrsequential.go`

- 通过`loadPlugin`得到`mapf`和`reducef`

步骤：

读入文件内容，将文件名和文件的内容组成的字符串传入reduce函数，生成键值对，讲所有键值对拼接成一个数组，作为中间值`intermediate`。

把`intermediate`根据键排序。

根据排序的结果，相同的键挨在一起，所以可以直接统计出相同的键对应的那些值。把这些值拼成一个数组`values`，然后连同值一起传给`reducef`。得到输出。