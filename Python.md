# Python
## 书籍
## 笔记
### 1. GIL线程全局锁

线程全局锁（Global Interpreter Lock），即Python为了保证线程安全而采取的独立线程运行的限制，说白了就是一个核只能在同一时间运行一个线程，对于io密集型任务，python的多线程起到作用，但对于cpu密集型任务，python的多线程几乎占不到任何优势，还有可能因为争夺资源而变慢。
见Python 最难的问题http://www.oschina.net/translate/pythons-hardest-problem

解决办法：多进程和下面的协程（协程也只是单CPU，但是能减小切换代价提升性能）。
