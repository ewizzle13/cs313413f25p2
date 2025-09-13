COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		With a small number of elements the results look the same, but performance differs as the list grows.
        ArrayList is faster for random access (get, set) because it uses an array under the hood.
        LinkedList is faster for frequent insertions or removals at the beginning or middle because it only relinks nodes instead of shifting elements.

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

Removes the element at index 5 of the list.
		list.remove(Integer.valueOf(5)); // what does this one do?

Removes the first occurrence of the value 5 (the object) from the list.
TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

If replaced with list.remove(77) it will try to remove the element at index 77 instead of the value 77.
TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.

Each test was executed with REPS = 1,000,000 iterations.
Running times were measured using System.nanoTime() or System.currentTimeMillis() before and after the loop, subtracting start from end. Multiple runs were recorded for consistency.


	SIZE 10
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	SIZE 100
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	SIZE 1000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	SIZE 10000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  val1 val2 val3 val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: val1 val2 val3 val4 val5 val6
		testArrayListAccess:     val1 val2 val3 val4 val5 val6
        testLinkedListAccess:    val1 val2 val3 val4 val5 val6

	listAccess - which type of List is better to use, and why?

    ArrayList is better, because access by index is O(1). In LinkedList, access by index is O(n) since it requires traversing nodes.
	listAddRemove - which type of List is better to use, and why?

	LinkedList is better when repeatedly adding or removing elements at the beginning or middle, because it just relinks nodes (O(1)).
ArrayList is slower in these cases because it must shift all subsequent elements (O(n)).