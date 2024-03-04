# JavaTips
Java开发实用小技巧

1. 使用final关键字
   当一个变量的值在初始化后不再改变时，用final修饰，这不仅可以提高代码可读性，也有助于编译器进行优化。
   ```
    public class Constants {
        public static final String CONSTANT_NAME = "JAVA-TIPS";
        public static final int MAX_ATTEMPTS = 3;
   }
   ```
