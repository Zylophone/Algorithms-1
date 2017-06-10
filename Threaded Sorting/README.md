Java threaded sorting:

The program sorts a large set of random numbers
 * in two different ways,
 * 1) With Java's collections.sort
 * 2) Use threads equal to the number of processors available for the JVM.
 
  Have test ran the script with 20 Million random numbers.
  Threaded sort performed 4X compared to Collections sort on MacBook Pro.
  
  > Overview:
  * The program splits the input random numbers into range buckets.
  * Each range bucket is sorted in a different thread.
  * The callable thread returns the sorted list.
  * Sorted range buckets are merged to form the final list of sorted numbers.
  
  *Finally both the sorted lists are compared for sorting validation.*
  
  Uses Java's Executor framework for tasks submission. 