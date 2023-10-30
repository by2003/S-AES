# 项目简介

本项目包含SAES加解密工具、中间相遇攻击工具和CBC操作模式下的加解密工具 。
SAES加解密工具用于进行二进制和ASCII字符串的加密和解密操作。
中间相遇攻击破解工具提供了中间相遇破解功能和破解时间可视化功能。
CBC操作模式下的加解密工具提供加解密长密文的服务。

# 安装说明

要使用S-AES，您需要执行以下安装步骤：
* 确保您的计算机上已安装Java运行时环境（JRE）。
* 下载S-AES的源代码或可执行JAR文件。您可以从项目的GitHub存储库获取它。
* 如果您下载的是源代码，请在命令行或集成开发环境中编译并运行工具。如果您下载的是可执行JAR文件，请直接运行它。

# 代码结构：

* SAES.java实现了S-AES算法
* CBC.java实现了CBC模式下的S-AES算法
* GUI.java是基于S-AES算法的加解密工具，它提供用户交互界面，可以实现二进制、ASCII字符串的加密、解密操作，同时可以选择单重、双重K1、双重K1+K2、三层K1+K2、三层K1+K2+K3多种加解密方法；
* MiddleMeetAttackGUI同样是基于S-AES算法的中间相遇攻击破解工具，提供用户交互界面，用户可以选择明密文对的数量、可以选择加密方式，然后输入明密文对来破解密钥。同时，用户可以了解破解的时间。
* CBC_GUI是基于CBC模式下S-AES算法的长密文对加解密工具，它提供用户交互界面，用户输入长二进制明文或密文，选择加或解密即可得到结果。

# 使用指南

## GUI.java

S-AES加解密工具允许用户对二进制或字符串进行加密和解密操作。以下是GUI.java的使用指南：

1. 运行加解密工具GUI.java。
2. 在文本框中输入您要加密的明文。
3. 选择明文的类型是二进制数字或ASCII字符串。
4. 在 "密钥" 文本框中输入10位二进制密钥。
5. 选择加密或解密操作。
6. 选择加密模式，在单重、双重K1、双重K1+K2、三层K1+K2、三层K1+K2+K3多种加解密方法中选择。
7. 点击“执行”按钮。
8. 结果将显示在 "结果" 区域中。

## MiddleMeetAttackGUI.java

MiddleMeetAttackGUI是一个用于中间相遇破解S-AES密钥的工具。以下是使用MiddleMeetAttackGUI的使用指南：

1. 运行MiddleMeetAttackGUI.java。
2. 从下拉框中选择要使用的明文密文对的数量（1到5对）。
3. 每对明文密文输入16位二进制数字。
4. 选择输入明密文对的加密方式以缩小查找范围（双重K1、双重K1+K2）。
5. 单击 "查找密钥" 按钮开始暴力破解过程。
6. 结果区域将显示已找到的密钥列表。
7. 在完成暴力破解后，工具将显示破解所需的总时间。

## CBC_GUI.java

基于CBC模式下的S-AES加解密工具允许用户对长二进制进行加密和解密操作。以下是CBC_GUI.java的使用指南：

1. 运行加解密工具CBC_GUI.java。
2. 在文本框中输入您要加密的明文。 
3. 在 "密钥" 文本框中输入16位二进制密钥。 
4. 选择加密或解密操作。 
5. 点击“执行”按钮。 
6. 结果将显示在 "结果" 区域中。

# 示例

以下是一些使用S-AES的示例：

## 示例 1：S-AES加解密工具

* 输入明文或密文：1111001011110010
* 密钥：10101010101010101010
* 选择加密或解密，包括单重、双重K1、双重K1+K2、三层K1+K2、三层K1+K2+K3
* 结果显示在 "结果" 区域中。

## 示例 2：S-AES加解密工具

* 输入明文或密文：abcd
* 密钥：10101010101010101010
* 选择加密或解密，包括单重、双重K1、双重K1+K2、三层K1+K2、三层K1+K2+K3
* 结果显示在 "结果" 区域中。

## 示例 3：中间相遇攻击

* 输入多对明文密文，例如10101010101010101010，00101111101010001010
* 选择加密方式“双重K1+K2”
* 单击 "查找密钥" 按钮
* 工具将尝试暴力破解密钥并显示已找到的密钥列表和破解所需的总时间。

## 示例 4：S-AES加解密工具

* 输入明文或密文：101010101010101010101010101010101010101010101010101010101010
* 密钥：00101111101010001010
* 选择加密或解密
* 结果显示在 "结果" 区域中。

# 配置说明

S-AES通常不需要额外的配置。

