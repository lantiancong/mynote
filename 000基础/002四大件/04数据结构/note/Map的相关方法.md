# Map的相关方法

```java
Map<String, Integer> map = new HashMap<>();
map.put("apple", 10);  // 添加新键值对，返回null
map.put("apple", 20);  // 覆盖旧值，返回10

//根据键获取对应的值。若键不存在，返回null。
int count = map.get("apple");  // 返回20

map.remove("apple");  // 返回20，map中不再包含该键,若键不存在，返回null。
```

```java
//boolean containsKey(Object key)
//boolean containsValue(Object value)
    
//判断 Map 中是否包含指定的键，返回true或false。
map.containsKey("apple");  // 若已删除，返回false

//int size()
//boolean isEmpty()
```



```java
//Set<K> keySet()
//返回所有键的集合（Set类型），可用于遍历所有键。
Set<String> keys = map.keySet();
for (String k : keys) {
    System.out.println(k);  // 遍历所有键
}

//Collection<V> values()
//功能：返回所有值的集合（Collection类型），可用于遍历所有值。

//Set<Map.Entry<K, V>> entrySet()
//功能：返回所有键值对（Entry对象）的集合，每个Entry包含getKey()和getValue()方法，用于高效遍历键值对。
Set<Map.Entry<String, Integer>> entries = map.entrySet();
for (Map.Entry<String, Integer> entry : entries) {
    System.out.println(entry.getKey() + ":" + entry.getValue());
}
```

### JDK 8+ 新增的实用方法

```java
//V getOrDefault(Object key, V defaultValue)
//功能：根据键获取值，若键不存在则返回指定的默认值（避免null处理）。
// 键"banana"不存在，返回默认值0
int num = map.getOrDefault("banana", 0);  


void forEach(BiConsumer<? super K, ? super V> action)
功能：使用 Lambda 表达式遍历键值对，简化循环代码。
map.forEach((k, v) -> System.out.println(k + ":" + v));
```

