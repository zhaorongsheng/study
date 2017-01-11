## scala学习

### future学习
scala的并发处理能力，是通过两种方式实现：future和actor。Future在2.10.0版本中引入，并向后兼容到2.9.3。简单来讲，future是多线程的一种实现方式，可以有返回值，可以有回调函数。
- `scala.concurrent`里的`Future[T]`是一个容器类型，代表返回值类型为`T`的计算。当一个future完成时，可能结果是值，也可能结果为异常（异常／超时）。
- Future中的值是不可便的，只能写一次，写完后，就不可更改。
- `Future`和`Promise`是成对出现的，Future中的值，是Promise设置的，只能设置一次。
- 可以设置`ExecutionContext`，即Future运行的容器，可以使用java的`ExecutorService`实现：`ExecutionContext.fromExecutor(Executors.newFixedThreadPool(2))`

[scala future相关参考](https://windor.gitbooks.io/beginners-guide-to-scala/content/chp8-welcome-to-the-future.html)

#### actor学习


### 参考文档
