#### Java basics

Advantages:

- simple (automatic memory collection and garbage collection)
- oo
- rich api resources

Disadvantages:

- slow performance
- No control over gabbage collection
- more memory consuming

abstract vs interface

- abstract can have non-final (or non-static) variables, interface needs to be final (static)
- abstract can have non-abstract/abstract method where interface can only have abstract method
- all members in interface are public by default, abtarct can have private, protected

abstraction: hiding the implementation deails from the user

Polymorphism: 

- an object can take on many forms, a parent class repference is used to refer to a child class object

- ```java
  public interface Vegetarian{}
  public class Animal{}
  public class Deer extends Animal implements Vegetarian{}
  ```

  ```java
  Deer d = new Deer();
  Animal a = d;
  Vegetarian v = d;
  Object o = d;
  ```

Inheritance:

- one class acquire the properties of another

- ```java
  class Super {
     .....
     .....
  }
  class Sub extends Super {
     .....
     .....
  }
  ```

encapsulation

- wrapping the data and code acting on the data together as a single unit 
- data hiding
- Declare the valribale as private, provide public setter and getter method

Arrays (int[] nums)

- nums.length
- cannot use contains
- Sort: Arrays.sort(nums)
- Collections.sort()
- Collections.reverse()

List

- Length = l.size()
- return new ArrayList<>(map.values()); //result we want list of list

Queue

- Queue.offer (); add
- Queue.poll(); get

String

- s.length();

- s.charAt( int i)

- 

- ```java
              char[] ca = string.toCharArray();
              Arrays.sort(ca);
              String newString = String.valueOf(ca);
  ```

map

- map.putIfAbsent(key, new Arraylist<>())
- map.get(key).add(newValue)
- map.keySet()

others:

- Integer.toString(int)
- StringBuilder sb
  - sb.toString()
- List<String> result = new ArrayList();
- Result.add(element)
- hashMap.getOrDefault(key, 0)+1;
- int[] count = new int[26];
- 

Matrix 

- int\[\][] width = int\[0\].length depth = matrix.length
- if (matrix == null || matrix.length == 0 || matrix[0].length == 0) 

priorityQueue

- queue that can be put using custom comparator when initializing
- Queue<Integer> queue = new PriorityQueue<>((a,b) -> map.get(b) - map.get(a))
- a pq that based on the values in a map in decesding order
- Queue<String> queue = new PriorityQueue<>(
  ​            (a,b) ->map.get(a).equals(map.get(b))?
  ​        a.compareTo(b) : map.get(b) - map.get(a)); //if not condition for pq



## Questions

#### Algorithms

1. Given an 2d array of numbers that is sorted in both rows and columns, how would you find if a number is in the array or not.  

   - assume (10, 20, 30) (20, 30, 40)

   - start from top right most if n<target move down
   - if n> target move left
   - else found

2. Given a tree find out whether is a BST or not.  

   - recurse check if binary tree with narrowing max and min

3. find kth largest element in an unsorted array

   - quickselect

     ```java
     QuickSelect(A, k)
       let r be chosen uniformly at random in the range 1 to length(A)
       let pivot = A[r]
       let A1, A2 be new arrays
       # split into a pile A1 of small elements and A2 of big elements
       for i = 1 to n
         if A[i] < pivot then
           append A[i] to A1
         else if A[i] > pivot then
           append A[i] to A2
         else
           # do nothing
       end for
       if k <= length(A1):
         # it's in the pile of small elements
         return QuickSelect(A1, k)
       else if k > length(A) - length(A2)
         # it's in the pile of big elements
         return QuickSelect(A2, k - (length(A) - length(A2))
       else
         # it's equal to the pivot
         return pivot
     ```

   - O(n)

4. guessing game

   - divide and conquer

5. binary arithmetic on strings

   - ```java
     static` `String addBinary(String a, String b) 
         ``{ 
              
             ``// Initialize result 
             ``String result = ``""``;  
              
             ``// Initialize digit sum 
             ``int` `s = ``0``;          
      
             ``// Traverse both strings starting  
             ``// from last characters 
             ``int` `i = a.length() - ``1``, j = b.length() - ``1``; 
             ``while` `(i >= ``0` `|| j >= ``0` `|| s == ``1``) 
             ``{ 
                  
                 ``// Comput sum of last  
                 ``// digits and carry 
                 ``s += ((i >= ``0``)? a.charAt(i) - ``'0'``: ``0``); 
                 ``s += ((j >= ``0``)? b.charAt(j) - ``'0'``: ``0``); 
      
                 ``// If current digit sum is  
                 ``// 1 or 3, add 1 to result 
                 ``result = (``char``)(s % ``2` `+ ``'0'``) + result; 
      
                 ``// Compute carry 
                 ``s /= ``2``; 
      
                 ``// Move to next digits 
                 ``i--; j--; 
             ``} 
              
         ``return` `result; 
         ``} 
     ```

6. perfomance analysis if binary tree is implemented in linkedlist or array

   - Linked lists insertions and deletions are much less expensive than when done in arrays (think of array element shifts you have to do to fulfill those two operations.
   - Linked lists offer flexible size, while arrays do not; you will have to handle array expansion when data does not fit within initial array size.
   - Arrays offer random access, while linked lists do not; e.g. when dealing with an array implementation of a full or complete binary tree, we can easily compute the indices of any node in the tree.

7. Given a list of words, group all the anagrams

   - Idea: create two arrays: index array and words array

     ​	copy words to word array, initilize index array

     ​	sort individual words in words array index does not change

     ​	sort the words compare individual words 

     ​	use hash map to print

8. Given a list of words, find the longest common prefix between them.  

   ```java
      public String longestCommonPrefix(String[] strs) {
          if (strs == null || strs.length == 0) return "";
           for (int i=0; i<strs[0].length(); i++) {
               for (int j=1; j<strs.length; j++) {
                   if (i>=strs[j].length() || strs[j].charAt(i) != strs[0].charAt(i)) {
                       return strs[0].substring(0,i);
                   }
               }
           }
           return strs[0];
       }
   ```

1. Given a large log file, return or print the ten most visited URLs. 
2. check palindrome
3. reverse linked list
4. get the k first element of a list
5. change a number into any arbitraty base 


#### Web

1. what is ssl:
   - Secure socket layer (http**S**)
   - is the standard security technology for establishing an encrypted link between a web server and a browser. This link ensures that all data passed between the web server and browser remain private
2. protocol used to transfer message
3. what port does http use
4. what protocol is used by http



#### Linux / OS

1. kill command
   - kill a process using the kill signal and PID given by the user
   - Kill -9 PID / kill -SIGKILL PID
2. generator
3. deadlock
4. process and thread where are shared where not

#### SQL

1. move rows from one table to another

   - ```INSERT INTO table_A SELECT * FROM table_B WHERE key = 'blah';```

2. which one of the following describe inner join A. intersection B. A Union B

   - intersection

     ```sql
     SELECT * 
     FROM table1 INNER JOIN table2 
     ON table1.column_name = table2.column_name;
     ```

3.  How to retrieve a row from a table in SQL

#### Random

1. \# of bits to represent octal 
   - 3 octal -> 8
2. Max value that can be represented by undigned int
   - FFFF FFFF(16)
   - 1111 1111 1111 1111 1111 1111 1111 1111 (32bit)