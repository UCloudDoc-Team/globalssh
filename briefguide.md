# 使用指南

## 如何创建

### 云主机产品入口创建

1.进入云主机/EIP产品列表，点击GlobalSSH的“S”灰色图标  
![](/images/globalssh0126-1.png)

2.选择GlobalSSH的版本  
![](/images/globalssh-create1.png)

3.填写服务器IP、靠近区域、服务器端口等信息，点击确定按钮创建  
![](/images/createglobalssh-uhost2.png)


### GlobalSSH入口创建

1.进入**网络加速**产品大类下SSH加速通道GlobalSSH入口，点击**创建**按钮  

2.输入需要加速的服务器IP，选择可覆盖你服务器物理位置的区域选项，输入服务器端口号并创建。  
如：假设服务器在华盛顿，选择华盛顿选项即可；假设服务器在曼谷，可选择能覆盖曼谷区域的香港或新加坡选项  
![](/images/globalssh-create.png)


入门版GlobalSSH采用共享IP的方式，不同的实例会分配不同的端口用于SSH连接，因此GlobalSSH端口与服务器端口不一致。

## 如何使用

创建成功后，会生成一个ipssh.net后缀域名  
注：ipssh.net为GlobalSSH产品的正式域名，部分ucloudgda.com结尾的加速域名仍可使用  

> 禁止加速域名直接提供HTTP/HTTPS访问。

**Linux系统**  

在远程登录工具中，使用**加速域名**进行登录。

命令行登录示意（CentOS）:  
```
ssh {用户名}@{AcceleratingDomain}
```
免费版：
```
ssh {用户名}@{AcceleratingDomain} -p ${GlobalSSHPort}
```

友情提示，当您使用其他友商云主机或不同linux发行版，注意SSH登录的用户名可能不同

!> 风险提示：UCloud免费为每个加速IP提供不超过 3 Gbps的基础攻击防御（不同地域支持的最大免费防护流量不同），当加速实例遭受DDoS攻击超过基础防护阈值后，UCloud会对加速区域入口IP采取封堵措施，加速实例将会回源处理。若您的加速实例持续遭受DDoS攻击，产品方保留回收实例权利。
