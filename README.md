# thingsboard3.5 Setting for windows

## 1. thingsboard3.5的maven配置文件

thingsboardSettings.xml能够正常配置，如果配置失败，就选择thingsboardAliSettings.xml
## 2. 使用说明

#### ①maven版本3.9.3
#### ②使用前根据自己的需要对配置文件中的仓库地址进行更改，`<localRepository>G:\maven-3.9.3\repository\thingsboard</localRepository>`，位置在文件的第55行
#### ③在thingsboard源码的目录地址下，运行指令 `mvn clean install -DskipTests --settings ***`, ***处为maven配置文件的存放地址, eg: `mvn clean install -DskipTests --settings G:\maven-3.9.3\conf\thingsboardSettings.xml`

-----

## 1. 使用Docker安装postgres

Docker安装 参照: `https://www.cnblogs.com/5ishare/p/7259257.html`

```
# pull postgres image of TAG version, eg. docker pull postgres:14.2
docker pull postgres:TAG

# create container
docker run --name postgres -e POSTGRES_PASSWORD=postgres -p 5432:5432 -d postgres:TAG
```

## 2. 使用DBeaver连接postgres

参照: `https://blog.csdn.net/qq_38983728/article/details/131730001  的步骤1~2`
`ATTATION: 最后要创建一个名为thingsboard的数据库，并且把其他的数据库全部删掉，只留下它`

## 3. 安装必要的数据文件

终端cd到`...\application\target\windows`的绝对路径，然后执行`install_dev_db.bat`,显示successfully后即可！


`over`
