Leetcode

Arrays (int[] nums)

- nums.length
- cannot use contains
- Sort: Arrays.sort(nums)
- Collections.sort()
- Collections.reverse()

List

- Length = l.size()

Queue

- Queue.offer (); add
- Queue.poll(); get

String

- s.length();
- s.charAt( int i)

others:

- Integer.toString(int)
- StringBuilder sb
  - sb.toString()
-  List<String> result = new ArrayList();
- Result.add(element)
- hashMap.getOrDefault(key, 0)+1;
- int[] count = new int[26];

priorityQueue

- queue that can be put using custom comparator when initializing
- Queue<Integer> queue = new PriorityQueue<>((a,b) -> map.get(b) - map.get(a))
- a pq that based on the values in a map in decesding order