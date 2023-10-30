# 接口文档

## SAES.java接口文档

SAES类实现了S-AES算法的加密和解密操作。

### 方法

**1. public static int[] encrypt(int[] plaintext, int[] key)**

* 描述：对给定的明文使用S-AES算法进行加密。
* 参数：
* plaintext：包含16位二进制明文的数组。
* key：包含16位二进制密钥的数组。
* 返回：包含16位二进制密文的数组。

**2. public static int[] decrypt(int[] ciphertext, int[] key)**

* 描述：对给定的密文使用S-AES算法进行解密。
* 参数：
* ciphertext：包含16位二进制密文的数组。
* key：包含16位二进制密钥的数组。
* 返回：包含16位二进制明文的数组。


## CBC.java接口文档

CBC 类实现了Cipher Block Chaining (CBC) 模式的加密和解密操作。

### 方法
**1. public static int generateIV()**
* 描述：生成一个16位的随机初始化向量（IV）。
* 参数：无
* 返回：一个16位的随机二进制整数作为初始化向量（IV）。

**2. public static String encrypt_CBC(String plaintext, int key, int IV)**
* 描述：使用CBC模式对给定的明文进行加密。
* 参数：
* plaintext：要加密的明文，以16位二进制字符串的形式提供。
* key：16位二进制密钥。
* IV：16位二进制初始化向量（IV）。
* 返回：包含16位二进制密文的字符串。

**3. public static String decrypt_CBC(String ciphertext, int key, int IV1)**
* 描述：使用CBC模式对给定的密文进行解密。
* 参数：
* ciphertext：要解密的密文，以16位二进制字符串的形式提供。
* key：16位二进制密钥。
* IV1：16位二进制初始化向量（IV）。
* 返回：包含16位二进制明文的字符串。


## GUI.java接口文档

GUI类是基于S-AES算法的加解密工具的用户界面。

### 构造方法

**1. public GUI()**
描述：创建一个新的GUI实例。
参数：无。
返回：无。

### 公共方法

**1. public static void main(String[] args)**
* 描述：启动加解密工具的用户界面。
* 参数：args：命令行参数，用于启动应用程序。
* 返回：无。

**2. private void encryptText()**
* 描述：使用S-AES算法对用户输入的文本进行加密。
* 参数：无。
* 返回：无。

**3. private void decryptText()**
* 描述：使用S-AES算法对用户输入的文本进行解密。
* 参数：无。
* 返回：无。

**4. private boolean validateInput()**
* 描述：验证用户输入的文本和密钥是否有效。
* 参数：无。
* 返回：如果输入有效则返回true，否则返回false。


## MiddleMeetAttackGUI.java接口文档

MiddleMeetAttackGUI类是基于S-AES算法的密钥中间相遇攻击破解工具的用户界面。

### 构造方法

**1. public MiddleMeetAttackGUI()**
* 描述：创建一个新的MiddleMeetAttackGUI实例。
* 参数：无。
* 返回：无。

### 公共方法

**1. public static void main(String[] args)**
* 描述：启动密钥破解工具的用户界面。
* 参数：
* args：命令行参数，用于启动应用程序。
* 返回：无。

**2. private void updateInputPairsPanel()**
* 描述：根据用户选择的明密文对数量更新输入面板。
* 参数：无。
* 返回：无。

**3. private void findKey()**
* 描述：执行密钥破解操作，查找可能的密钥。
* 参数：无。
* 返回：无。

**4. private String formatTime(long nanos)**
* 描述：将时间格式化为时间字符串。
* 参数： 
* nanos：要格式化的纳秒时间。
* 返回：格式化后的时间字符串。

**5. private int[] stringToArray(String str)**
* 描述：将二进制字符串转换为整数数组。
* 参数： 
* str：要转换的二进制字符串。
* 返回：包含二进制位的整数数组。

**6. private String arrayToString(int[] arr)**
* 描述：将整数数组转换为二进制字符串。
* 参数： 
* arr：要转换的整数数组。
* 返回：包含二进制位的字符串。

**7. private int[] intToBits(int n)**
* 描述：将整数转换为10位二进制位的整数数组。
* 参数： 
* n：要转换的整数。
* 返回：包含10位二进制位的整数数组。

## CBC_GUI.java接口文档

CBC_GUI 类实现了一个用于执行CBC模式加密和解密操作的图形用户界面。

### 构造函数

**public CBC_GUI(int IV)**
* 描述：构造一个CBC模式加解密工具的图形用户界面窗口。
* 参数：
* IV：用作初始化向量（IV）的16位整数。

### 私有方法：

**1. private void handle(int IV)**
* 描述：处理用户的输入，执行加密或解密操作，并在结果文本区域显示结果。
* 参数：
* IV：用作初始化向量（IV）的16位整数。

**2. private String bitsToString(List<Integer> bits)**
* 描述：将二进制位列表转换为二进制字符串。
* 参数：
* bits：包含二进制位的整数列表。
* 返回：二进制字符串。

**3.　private String bitsToAsciiString(List<Integer> bits)**
* 描述：将二进制位列表转换为ASCII字符串。
* 参数：
* bits：包含ASCII字符的整数列表。
* 返回：ASCII字符串。