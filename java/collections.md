# Collections

## Interfaces

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
- range view: subSet(E fromElement, E toElement); headSet(E toElement); tailSet(E fromElement);
- endpoints: first(); last();
- Comparator access: Comparator<? super E> comparator();

SortedMap
- range view: SortedMap<K, V>  subMap(K fromKey, K toKey); headMap(K toKey); tailMap(K fromKey);
- endpoints: Key<K> firstKey(); lastKey();
- Comparator access: Comparator<? super K> comparator();


