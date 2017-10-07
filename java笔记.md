- [HashMap深度解析(一)](http://blog.csdn.net/ghsau/article/details/16843543)
Object对象的两个方法
- hashCode()
- equales()
HashMap<K,V> 实现Map<K,V>接口，集合类的一种
插入时，首先使用K的hashCode()，
  - 没有碰撞，直接插入
  - 如果出现碰撞，然后使用equals()
    - 如果K相等，则替换V，
    - 如果K值不等，则在原K值处插入单链表
    
# 设计模式
## 单例模式

```java
public class Singleton {
        private static Singleton instance = new Singleton();
        public static Singleton getInstance() {
                return instance;
        }
}
```
## 门面模式
把一系列复杂的处理过程封装在门面类的内部，对外仅提供统一的函数，调用这不用关心函数内部的处理过程。
门面函数的修改对调用者都是透明的，不影响调用程序的使用。

