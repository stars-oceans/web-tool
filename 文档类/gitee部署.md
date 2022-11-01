1.背景
1.Gitee（GitHub） Pages 服务作为一个页面容器，可以说是非常方便了。我们可以在上面免费部署前端项目。
2.并且同时获得一个附带.gitee.io（github.io）的网址。
3.其他优点就不再赘述，可自行百度。
2.Gitee Pages的介绍
具体可以看这个网址Gitee Pages官方介绍
3.上传自己的项目到Gitee上。
点击项目导航栏中的服务 --> Gitee Pages


如果是静态项目，此处不再说啥，直接构建，你的项目中有index.html(主入口)就可以
4.如果你的是Vue项目(重点讨论)
首先，根据官方指示


在项目路径中添加.spa文件


原理，我不是很清楚，应该是给Nginx做一个标识作用吧。
5. 本地`build
在构建前，一定要注意修改两个地方
一、将build.js文件中的console.log全部注释

二、将config/index.js中的assetsPublicPath值改为./或图中的英文指示改为你的项目名称加/如： '/ltz/'
解决JS访问不到的问题。
注意，此处修改的assetsPublicPath为build对象中的！



```js
module.exports = {
  
  // 部署
  publicPath:'/toutiao/',
 
};
```



三、打开build/utils.js文件（解决CSS/字体找不到问题）
在如下位置添加 publicPath: '../../'

在本地运行npm run build，得到`dist
`

7.将build得到的文件，上传到你git仓库中。
8.点击项目导航栏中的服务 --> Gitee Pages
9.开始构建

选择你的分支，如果只有一个分支，就选master
选择部署目录，本文中，build后的文件全部都在dist目录下，所以，填入dist。
如果，你发现，构建后，css\js\img等文件，报了404异常，请看本文第5步 -> 二\三
————————————————
版权声明：本文为CSDN博主「LitongZero」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/LitongZero/article/details/88207833