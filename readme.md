# notes

## read/write lock 

https://www.cnblogs.com/fsmly/p/10721433.html

公平锁：Threads acquire a fair lock in the order in which they requested it公平锁，就是很公平，在并发环境中，每个线程在获取锁时会先查看此锁维护的等待队列，如果为空，或者当前线程是等待队列的第一个，就占有锁，否则就会加入到等待队列中，以后会按照FIFO的规则从队列中取到自己
非公平锁：a nonfair lock permits barging:threads requesting a lock can jump ahead of the queue of waiting threads if the lock happens to be available when it is requested.
非公平锁比较粗鲁，上来就直接尝试占有锁，如果尝试失败，就再采用类似公平锁那种方式。

作者：名字是乱打的
链接：https://www.jianshu.com/p/b5969b6e0dc6
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

