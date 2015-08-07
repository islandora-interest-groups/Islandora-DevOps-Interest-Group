#Tuning
* Brad's Rule="50% of physical RAM to JVM"
* JAVA_OPTS="-Xloggc:/var/log/islandora/java/java_gc.log -XX:+PrintGCDetails -XX:+PrintGCTimeStamps -XX:ErrorFile=/var/log/islandora/java/java_error%p.log -Xms15g -Xmx15g -XX:MaxPermSize=1g -XX:+DisableExplicitGC -XX:+UseParallelGC -XX:+UseParallelOldGC"
* Parallel garbage collector provides one thread of garbage collection per processor, our server has eight (8), resulting in very high throughput, which is required for big data object ingests.  The single-threaded CMS collector was incapabible of bailing out the "old generation" memory space fast enough, resulting in Tomcat out of memory errors and total failure...

#Tips

#Tricks

* Real-time Java Heap Analysis 
```
#!/bin/sh
xyzzy=$(jps | awk '~/Bootstrap/{print }')
jmap -heap $xyzzy
```
