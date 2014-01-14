ProcessPool.h
=============

processpool


Example
----
```C++
const int WORKERS = 4;

ProcessPool<int> pool(WORKERS, [](int a){
		printf("process %d\n", a);
		return true;
	});

for(int i=0;i<1000;i++){
		pool.enqueue( i );
}
```
