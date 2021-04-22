# CS Theory Interview Questions

What is recursion and give an example using JavaScript?

> A recursive function is one that calls itself, as in this implementation of a merge sort.

````javascript
function merge(a, b) {
> return a.length == 0 ? b :
>           b.length == 0 ? a :
>           a[0] <= b[0] ? merge(a.slice(1), b).unshift(a[0]) :
>                                merge(b.slice(1), a).unshift(b[0]);
}
function sort(a) {
> const mid = Math.floor(a.length/2);
> return a.length <= 1 ? a : merge(sort(a.slice(0, mid)), sort(a.slice(mid+1));
}
````

What are types?  &#128077;&#127998;

> Types differentiate the kinds of objects manipulated by a program.  They can be built-in types such as number, string, and array, or they can be types defined by classes in an object-oriented language.

What are data structures?  &#128077;&#127998;

> Data structures provide representations for abstract data types.  For example, a list can be represented by an array or by a singly or doubly linked list.

What is an algorithm?  &#128077;&#127998;

> An algorithm is a set of steps for solving a problem, akin to a recipe for baking a cake or a detailed blueprint for building a house.

What is scope / lexical scope in JavaScript?

> The scope of an identifier in a program is the portion of the program in which references can be made to that identifier.  A lexical scope is one defined by the nesting of program elements (e.g., the body of a function definition or a loop).

What is polymorphism?

> Polymorphism is a mechanism for parameterizing class definitions.  For example, in TypeScript, `Set<T>` can be defined to be a set of objects of type `T` and instantiated as `Set<string>` or `Set<number>`.

What is encapsulation?  &#128077;&#127998;

> Encapsulation is a mechanism for hiding information (using private or protected variables) inside the definition of a class so as to make that information visible outside of the class's definition only by calling methods of the class.

What is a Linked List?  &#128077;&#127998;

> A linked list is a data structure that represents a one-dimensional array.  Each element in the list contains a value and a reference to the next element In the list.  JavaScript implements arrays as linked lists.

What is a Doubly Linked List?

> Each element in a doubly linked list contain an additional reference to the element that precedes it in the list.

What is a Queue?  &#128077;&#127998;

> A queue is a first-in first-out (FIFO) list, that is, a list with operations (enqueue and dequeue) for adding an element to the end of a list and removing one from the beginning.  JavaScript use a queue to manage events to be handled on a first-come, first-served basis.

What is a Stack?  &#128077;&#127998;

> A stack is a last-in first-out (LIFO) list, that is, a list with operations  (push and pop) for adding an element to the end of a list and removing one from the same end. Runtime systems use a call stack to maintain the values local to a series of nested function calls.

What is a Hash Table?  &#128077;&#127998;

> A hash table is a map from keys to values that stores entries in a set of buckets and locates the appropriate bucket for a key by applying a hash function to the key.  A good hash function distributes the entries evenly among the buckets.

What is a Heap?

> The word _heap_ has two different meanings.  It can be a specialized data structure (a kind of binary tree) used by the heap sort algorithm.  Normally it refers to runtime storage that contains objects not on the call stack (e.g., objects allocated by class constructors).

What is a Trie?  &#128078;&#127998;

> A trie is a special kind of search tree.  I would have to look up its definition.

What is a Tree?

> A tree is a data structure in which each element is related to a number of other elements called its children.  There is exactly one element, called the root of the tree, that is not the child of any other element.  Each other element has a single parent (i.e., is the child of a single element in the tree) and is a descendant of the root of the tree.  Trees have many important applications to searching, sorting, parsing, generating fractal patterns, solving puzzles, and playing games of strategy.

What is a Binary Search Tree?

> A binary search tree is an ordered tree in which every element has a label and zero or two children.  The label of an element's left child is less than or equal to the element's label, which is less than or equal to the label of its right child.
>
> &#128078;&#127998; This is getting to be a little too esoteric for an interview.

What is a Disjoint Set?  &#128078;&#127998;

> A disjoint set is a data structure that partitions a set into disjoint subsets.

What is a Bloom Filter?  &#128078;&#127998;

> I would have to look up the definition.

Demonstrate Bubble Sort and explain when you might use it?

> A bubble sort is an algorithm that is easy to code, but has no redeeming features other than being stable and very efficient when applied to a list that is already sorted.  In the first pass over a list, it bubbles the largest element to the end of the list by exchanging pairs of elements that are out of order.  In later passes, it bubbles increasingly smaller elements to their proper places in the list.  It is not very efficient because it can cause elements of data to be moved many times.

Demonstrate Insertion Sort and explain when you might use it?

> Insertion sort successively removes elements from the list and inserts in the proper order in an initially empty linked list.  Insertion support performs better than merge sort or quicksort for short lists.

Demonstrate Merge Sort and explain when you might use it?

> Merge sort was shown above as a sample use of recursion.  It requires $O(n \cdot log(n))$ time in the worst case, whereas bubble sort and insertion sort require $O(n^2)$ time.  Its speed, and the fact that it works well when sorting large amounts of data on secondary storage, make it an attractive algorithm.  Some implementations of JavaScript use it to implement array.sort.  It is also a stable sort (that is, when used to sort records with several fields, using one field as the key, it preserves the order of records that have equal keys).

Demonstrate Quicksort and explain when you might use it?

> Quicksort is another recursive sort.  It is faster than merge sort in the average case, but requires $O(n^2)$ in the worst case.  Some implementations of JavaScript use it to implement array.sort.  It is not stable.
>
> &#128078;&#127998;  Questions about quicksort and merge sort are fair game because some implementations of JavaScript use one for `array.sort` and some use the other.  Hence it's helpful to know how they differ and why one might be chosen over the other.  However, I don't think it's reasonable to ask for a demonstration of how quicksort works.

Auto Pass
