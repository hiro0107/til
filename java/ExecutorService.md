# ExecutorService

ExecutorServiceのshutdownは新規の実行を受け付けないだけで、受付済みの実行は続ける。ExecutorService#awaitTerminationで時間付きで待つ。

参考) http://javazuki.com/articles/executor-framework-usage.html
