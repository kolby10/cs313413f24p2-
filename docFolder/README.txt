** TestIterator.java
try with a LinkedList - does it make any difference?


TODO what happens if you use list.remove(Integer.valueOf(77))?
It could throw an exception. This is due to list.remove modifying the iterators list
outside of the iterator itself. Using i.remove() is a better choice as it specifies what
specific index that iterator is currently subjecting.

* TestIterator.java 4/4 passed

** TestList.java
 list.remove(Integer.valueOf(5)); // what does this one do?
 this line removed the value that is stored at index 5

 TODO also try with a LinkedList - does it make any difference?
May cause a small increase in compiling time, but no apparent difference in the output the
code provides.

* TestList.java 12/12 passed

** TestPerformance.java
 TODO run test and record running times for SIZE = 10, 100, 1000, 10000, ...
 LinkedListPerformance()
  10 = 40ms
  100 = 45ms
  1000 = 435ms
  10000 = 5 sec, 534ms
  100000 = 56 sec, 39ms
  1000000 = 60+secs

 ArrayListPerformance()
  10 = 34ms
  100 = 44ms
  1000 = 226ms
  10000 = 1 sec, 994ms
  100000 = 21 sec, 858ms


which of the two lists performs better as the size increases?

the ArrayList performs better as size increases, due to ArrayList having
a constant time of [O(1)], vs LinkedList's O(n).
As we increase size, the constant time of ArrayList beats LinkedList's
ever-increasing processing time.

TODO choose this value in such a way that you can observe an actual effect

    LinkedListPerformance()
    size 1000, reps = 1000000, 431ms
    size 1000, reps = 10000000, 4 sec, 88ms
    size 10000, reps = 1000000, 6 sec, 451ms
    size 10000, reps = 10000000, 52 sec, 92ms


    ArrayListPerformance()
    size 1000, reps = 1000000, 225ms
    size 1000, reps = 10000000, 2 sec, 132ms
    size 10000, reps = 1000000, 1 sec, 982ms
    size 10000, reps = 10000000, 19 sec, 671ms

    An increase of reps exponentially increases the processing time on
    both ArrayLists and LinkedLists


* TestPerformance.java 6/6 tests passed.