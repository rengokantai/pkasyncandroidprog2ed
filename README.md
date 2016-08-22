#### pkasyncandroidprog2ed
#####Chapter 1. Asynchronous Programming in Android
single main thread vs async:
On the left-hand side, the data download task occurs on the main thread, keeping the thread busy until the download data is finished.  
On the right-hand side, the asynchronous model will hand over the download data task to another background thread, 
keeping the main thread available to process any event coming from...  
The simultaneous execution of separate code paths that potentially interact with each other is known as concurrency.  
The simultaneous execution of subunits of work in parallel to complete one unit of work is known as parallelism.  
######Android thread model

######Concurrent package constructs
Thread Pools
```
Executors.newCachedThreadPool()
Executors.newFixedThreadPool (nThreads)
Executors.newSingleThreadPool():
```
######Service concurrent issues
- Started services  
Service that is started by startService() that can run definitively even if the component that started it was destroyed.
- Bound services  
Exists while at least one Android component is bounded to it by calling bindService()
######Started services issues
```
int onStartCommand(Intent intent, int flags, int startId)
```
######Service in a separate process
service tag
```
```
######Broadcast receiver concurrent issues  
The broadcast receivers are defined statically in the application manifest or dynamically via the
```
Context.registerReceiver().
```

#####Chapter 2. Performing Work with Looper, Handler
######Understanding Looper
access to the main thread's Looper instance
```
Looper mainLooper = Looper.getMainLooper();
```
