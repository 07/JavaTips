# JavaTips
## Java开发实用小技巧（ Version : JDK8 ）

1. 使用final关键字
   - 当一个变量的值在初始化后不再改变时，用final修饰，这不仅可以提高代码可读性，也有助于编译器进行优化。
   ``` java
   public class Constants {
        public static final String CONSTANT_NAME = "JAVA-TIPS";
        public static final int MAX_ATTEMPTS = 3;
   }
   ```

2. 理解并正确使用equals()与hashCode()
   - 在实现自定义类时，如果该类作为集合（如HashMap、HashSet）的键，需要同时重写equals()和hashCode()方法，以保证两个相等的对象具有相同的哈希码。

3. 避免NullPointerException
   - 使用Objects.requireNonNull()对可能为null的对象引用进行检查，并在抛出异常时提供有意义的消息。
   ``` java
   String str = Objects.requireNonNull(strInput, "Input string cannot be null");
   ```

4. 集合初始化时避免直接用new ArrayList()
   - 当创建集合时，尽可能使用Collections工具类提供的方法或者流式API初始化，这样可以一目了然地看到集合内容和大小。
    ``` java
   List<String> names = new ArrayList<>(Arrays.asList("Alice", "Bob", "Jack"));
   ```

5. 利用注解提高代码质量
   - 使用如@Override确保重写父类方法；使用@Deprecated标记过时的方法；使用@NonNull、@NotNull等进行非空检查（配合静态代码分析工具）。
