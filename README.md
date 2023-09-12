# thingsboard3.5 Setting for windows

## 1. thingsboard3.5的maven配置文件

thingsboardSettings.xml能够正常配置，如果配置失败，就选择thingsboardAliSettings.xml
## 2. 使用说明

#### ①maven版本3.9.3
#### ②使用前根据自己的需要对配置文件中的仓库地址进行更改，`<localRepository>G:\maven-3.9.3\repository\thingsboard</localRepository>`，位置在文件的第55行
#### ③在thingsboard源码的目录地址下，运行指令 `mvn clean install -DskipTests --settings ***`, ***处为maven配置文件的存放地址, eg: `mvn clean install -DskipTests --settings G:\maven-3.9.3\conf\thingsboardSettings.xml`

-----
