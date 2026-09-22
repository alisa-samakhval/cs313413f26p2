COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		No, the code behaves in the same way.

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			Removes a value at index 5

		list.remove(Integer.valueOf(5)); // what does this one do?

			Searches for the first element that equals 5 and removes it.

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			Exception message, you can't modify a list's structure this way.

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.

	SIZE 10
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  46ms 44ms 43ms 46ms val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: 55ms 60ms 57ms 54ms val5 val6
		testArrayListAccess:     64ms 58ms 60ms 55ms val5 val6
        testLinkedListAccess:    24ms 22ms 22ms 23ms val5 val6

	SIZE 100
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  80ms 54ms 80ms 63ms val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: 70ms 54ms 55ms 67ms val5 val6
		testArrayListAccess:     76ms 59ms 53ms 58ms val5 val6
        testLinkedListAccess:    44ms 34ms 31ms 31ms val5 val6

	SIZE 1000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  237ms 216ms 224ms val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: 61ms 63ms 53ms val4 val5 val6
		testArrayListAccess:     56ms 60ms 46ms val4 val5 val6
        testLinkedListAccess:    401ms 385ms 397ms val4 val5 val6

	SIZE 10000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  798ms 813ms 808ms val4 val5 val6  ... (fill these in in ms)
        testLinkedListAddRemove: 66ms 57ms 52ms val4 val5 val6
		testArrayListAccess:     69ms 57ms 69ms val4 val5 val6
        testLinkedListAccess:    809ms 821ms 863ms val4 val5 val6

	listAccess - which type of List is better to use, and why?

		ArrayList is better, access time stayed flat regardless of list size.
		ArrayList indexes directly into its backing array (O(1)) while LinkedList has to traverse node-by-node from the head (O(n)).


	listAddRemove - which type of List is better to use, and why?

		LinkesList os better, ArrayList add/remove at index 0 grew while LinkedList stayed flat.
		LinkesList has O(1), ArrayList O(n).