### TreeMap
TreeMap也实现了Map接口，它使用一种基于红黑树的数据结构来存储键值对。由于红黑树是一种有序结构，因此TreeMap中的键值对是按照键的自然顺序或者自定义比较器的顺序排列的。因此，可以使用TreeMap来实现对键值对的排序操作。

相比之下，TreeMap的插入、删除和查找元素的速度较慢，但是可以在需要排序的场景下使用。

```
TreeMap<String, Integer> unsortedMap = new TreeMap<>();
unsortedMap.put("A", 4);
unsortedMap.put("B", 1);
unsortedMap.put("C", 3);
unsortedMap.put("D", 2);

TreeMap<String, Integer> sortedMap = new TreeMap<>(new Comparator<String>()
    public int compare(String o1, String o2) {
        return unsortedMap.get(o1).compareTo(unsortedMap.get(o2));
    }
});

sortedMap.putAll(unsortedMap);

System.out.println("Sorted TreeMap: " + sortedMap);
===================================================
TreeMap<Integer, String> treeMap = new TreeMap<>(Comparator.reverseOrder());

treeMap.put(3, "Three");
treeMap.put(1, "One");
treeMap.put(2, "Two");

System.out.println("TreeMap: " + treeMap);
```
