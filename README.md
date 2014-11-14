##介绍
PHP实现 基于纯真IP库 根据IP地址查找对应的地理位置信息

####更新的版本
本库附带的`qqwry.dat`文件是`2014.11.5`更新的，如你需要更新的版本，请点击 [此处](http://www.cz88.net/) 到页面右上角下载更新的版本。dat文件官网5天一次更新。

####更高的性能

如果你需要更高的性能，请使用 [C扩展库](http://pecl.php.net/package/qqwry)

##安装

在你的`composer.json`中加入

```
"require": {
    "naux/iplocation": "dev-master"
},
```

##使用

```
use Naux\IpLocation\IpLocation;

$ip = new IpLocation();

$location = $ip->getlocation('119.75.217.56');
```

`$location`的内容如下

```
array (size=5)
  'ip' => string '119.75.217.56' (length=13)
  'beginip' => string '119.75.208.0' (length=12)
  'endip' => string '119.75.223.255' (length=14)
  'country' => string '北京市' (length=9)
  'area' => string '北京百度网讯科技有限公司BGP节点' (length=45)
```

####指定其他路径的纯真库dat文件

```
use Naux\IpLocation\IpLocation;

$ip = new IpLocation('/home/qqwry.dat');
```
