# SafeRM - 安全的递归文件删除

SafeRM是一个自定义的Shell脚本，用于在使用`rm -rf`命令时提供额外的保护层。它在删除文件和目录之前会提示用户确认，有助于防止意外数据丢失。

## 目录

- [安装](#安装)
- [使用](#使用)
- [支持场景](#支持场景)
- [许可证](#许可证)

## 安装

#### 要使用SafeRM，请按照以下安装步骤进行操作：

1. 将`saferm`文件复制到`/usr/local/bin`目录。
2. `chmod +x /usr/local/bin/saferm`
3. 编辑`~/.bashrc`文件，在其中添加`rm`的别名，如下所示：
   `alias rm='/usr/local/bin/saferm'`
4. 运行`source ~/.bashrc`
#### 或使用以下 cURL 或 Wget 一个命令解决
```shell
curl -o /usr/local/bin/saferm https://raw.githubusercontent.com/kookob/safe-rm/master/saferm && sudo chmod +x /usr/local/bin/saferm && echo "alias rm='/usr/local/bin/saferm'" >> ~/.bashrc && source ~/.bashrc
```
```shell
wget -P /usr/local/bin https://raw.githubusercontent.com/kookob/safe-rm/master/saferm && sudo chmod +x /usr/local/bin/saferm && sudo echo "alias rm='/usr/local/bin/saferm'" >> ~/.bashrc && source ~/.bashrc
```


## 使用
#### 验证`saferm`命令：  
   `alias rm`  
   如果您看到以下内容，这意味着`rm -rf`防止意外删除命令已生效。
   ```shell
   alias rm='/usr/local/bin/saferm'
   ```
## 支持场景
- rm -rf /
- rm -rf /*
- rm -rf * (根目录下)
- rm -rf ./* (根目录下)
- 根目录下其他系统目录的删除

## 许可
MIT
