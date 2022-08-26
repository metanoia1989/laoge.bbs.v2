# 老哥吧论坛

基于 [Xiuno BBS 4.0](https://github.com/jiix/xiunobbs)，原先用的是腾讯的 discuzQ，技术栈太复杂，搞的编译、部署、修改都很麻烦。  

xiuino bbs 开发文档 <https://www.yuque.com/xiand/xiunobbs/vydyme>     

## 安装使用
使用请下载发布版，集成较少插件。数据库请采用**utf8mb4**，安装完成后，请删除install目录。
插件和主题，直接上传到**plugin**目录中，后台插件中心开启。

## 伪静态设置
后台设置开启伪静态，添加对应的伪静态规则。

Nginx伪静态:
```lua
location ~* \.(htm)$ {
    rewrite "^(.*)/(.+?).htm(.*?)$" $1/index.php?$2.htm$3 last;
}
```

## 插件下载
临时插件仓库：[插件主题中心](https://github.com/jiix/plugins)
