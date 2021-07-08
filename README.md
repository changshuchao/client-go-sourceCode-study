# client-go-sourceCode-study
一些查看client-go的一些心得. enjoy it !



部分参考资料汇总:

[kubernetes client-go解析详细博客](https://www.cnblogs.com/charlieroro/p/10330390.html)

深入浅出系列： <https://so.csdn.net/so/search?q=%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BAkubernetes%E4%B9%8Bclient-go&t=blog&u=weixin_42663840>

- [深入浅出kubernetes之client-go的SharedInformerFactory](https://blog.csdn.net/weixin_42663840/article/details/81980022?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522161032580616780277058103%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fblog.%2522%257D&request_id=161032580616780277058103&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~blog~first_rank_v2~rank_v29-4-81980022.pc_v2_rank_blog_default&utm_term=%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BAkubernetes%E4%B9%8Bclient-go&spm=1018.2226.3001.4450)
- [深入浅出kubernetes之client-go的workqueue](https://blog.csdn.net/weixin_42663840/article/details/81482553?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522161032580616780277058103%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fblog.%2522%257D&request_id=161032580616780277058103&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~blog~first_rank_v2~rank_v29-2-81482553.pc_v2_rank_blog_default&utm_term=%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BAkubernetes%E4%B9%8Bclient-go&spm=1018.2226.3001.4450)
- [深入浅出kubernetes之client-go的Indexer](https://blog.csdn.net/weixin_42663840/article/details/81530606?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522161032580616780277058103%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fblog.%2522%257D&request_id=161032580616780277058103&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~blog~first_rank_v2~rank_v29-1-81530606.pc_v2_rank_blog_default&utm_term=%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BAkubernetes%E4%B9%8Bclient-go&spm=1018.2226.3001.4450)
- [深入浅出kubernetes之client-go的DeltaFIFO](https://blog.csdn.net/weixin_42663840/article/details/81626789?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522160993057616780266216649%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fblog.%2522%257D&request_id=160993057616780266216649&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~blog~first_rank_v2~rank_v29-3-81626789.pc_v2_rank_blog_default&utm_term=%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BAkubernetes%E4%B9%8Bclient-go&spm=1018.2226.3001.4450)
- [深入浅出kubernetes之client-go的SharedInformer](https://blog.csdn.net/weixin_42663840/article/details/81699303?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522161032580616780277058103%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fblog.%2522%257D&request_id=161032580616780277058103&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~blog~first_rank_v2~rank_v29-5-81699303.pc_v2_rank_blog_default&utm_term=%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BAkubernetes%E4%B9%8Bclient-go&spm=1018.2226.3001.4450)
- [client-go: Informer机制之reflector源码分析](https://blog.csdn.net/u013276277/article/details/108592288)

client-go和golang源码中的技巧: <https://www.cnblogs.com/charlieroro/p/11112526.html>



相关知识：[退避指数算法 ](https://www.jianshu.com/p/2663ec968668)    backoff