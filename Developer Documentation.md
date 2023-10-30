# 项目结构

S-AES项目包括以下主要组件：

* SAES.java: 实现S-AES算法的主要类，包括encrypt和decrypt方法。
* GUI.java: 基于S-AES算法的加解密工具的用户界面，用于进行加密和解密操作。
* SAESBruteGUI.java: 基于S-AES算法的密钥中间相遇破解工具的用户界面，用于破解密钥。
* CBC_GUI：CBC操作模式下加解密工具的用户界面，可以加解密长明密文。

# 开发环境要求

在开发S-AES项目之前，您需要确保以下软件和工具已安装在您的计算机上：

* Java开发工具包（JDK）：用于编译和运行Java代码。
* 集成开发环境（IDE）：例如Eclipse、IntelliJ IDEA或Visual Studio Code。

# 构建和运行

## 构建项目

要构建项目，您可以使用Java编译器。
`javac src/SAES.java src/CBC.java　src/GUI.java　src/MiddleMeetAttackGUI.java　src/CBC_GUI.java`

## 运行项目

运行SAES加解密工具GUI.java：
`java GUI`

运行中间相遇破解工具MiddleMeetAttackGUI.java：
`java MiddleMeetAttackGUI`

运行CBC模式下的SAES加解密工具CBC_GUI.java：
`java CBC_GUI`

# 代码规范

S-AES遵循Java的代码规范，包括适当的命名约定、注释、代码缩进等。

# 文档和注释

为了提高代码的可读性，S-AES添加了必要的注释以解释关键部分的功能和逻辑。