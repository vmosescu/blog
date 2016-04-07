# Collections

## Interfaces

### Collection
Collection
- Set (SortedSet): HashSet(hash table), TreeSet(ordered-cost), LinkedHashSet(orderd by insertion)
- List: ArrayList, LinkedList; subList(int fromIndex, int toIndex)
- Queue: 
  - nu neaparat FIFO
  - metode in doua forme: daca operatia esueaza arunca exceptie sau returneaza o valoare speciala
  - bounded: restrictioneaza numarul de elemente
- Deque: coada la ambele capete (first/last)

Map: HashMap, TreeMap, LinkedHashMap (+exemple)
- SortedMap

Ordonare
- Collections.sort(l); elementele din lista trebuie sa implementeze Comparable
- Collections.sort(l,comparator); daca nu vrem sa le ordonam natural

SortedSet

