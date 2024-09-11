TestIterator.java
try with a LinkedList - does it make any difference?


TODO what happens if you use list.remove(Integer.valueOf(77))?
test fails**




TestList.java
 list.remove(Integer.valueOf(5)); // what does this one do?
 this line removed the value that is stored at index 5

 TODO also try with a LinkedList - does it make any difference?
May cause a small increase in compiling time, but no apparent difference in the output the
code provides.

*TestList.java 12/12 passed

 TestPerformance.java
 TODO run test and record running times for SIZE = 10, 100, 1000, 10000, ...
 10 = 66ms
 100 = 84ms
 1000 = 529ms
 10000 = 6 sec, 527ms
 100000 = 1 min, 4 secs


TODO choose this value in such a way that you can observe an actual effect
size 100, reps = 1000000, 77 ms
size 100, reps = 10000000, 496 ms
size 100, reps = 100000000, 4 secs 432ms

which of the two lists performs better as the size increases?
**




