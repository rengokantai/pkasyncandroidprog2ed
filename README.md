#### pkasyncandroidprog2ed
#####Chapter 1. Asynchronous Programming in Android
single main thread vs async:
On the left-hand side, the data download task occurs on the main thread, keeping the thread busy until the download data is finished.  
On the right-hand side, the asynchronous model will hand over the download data task to another background thread, 
keeping the main thread available to process any event coming from...  
The simultaneous execution of separate code paths that potentially interact with each other is known as concurrency.  
The simultaneous execution of subunits of work in parallel to complete one unit of work is known as parallelism.  
######Android thread model
