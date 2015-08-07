Tuning

Tips

Tricks

* Real-time Java Heap Analysis 
`#!/bin/sh`
``xyzzy=$(jps | awk '~/Bootstrap/{print }')``
``jmap -heap $xyzzy``