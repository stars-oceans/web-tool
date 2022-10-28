一、在vue-cli脚手架项目中使用bootstrap3框架的步骤
1、先在项目中安装bootstrap和jquery

```js
npm i jquery bootstrap@3 -S
```


2、在main.js中引入bootstrap

```js
import 'bootstrap/dist/js/bootstrap.js'
import 'bootstrap/dist/css/bootstrap.css'
```


3、在项目的根目录新建一个配置文件vue.config.js,输入以下代码

```js
const webpack = require("webpack")
module.exports = {
	// 配置插件参数
	configureWebpack: {
		plugins: [
			// 配置 jQuery 插件的参数
			new webpack.ProvidePlugin({
				// 引入jquery
				$: 'jquery',
				jQuery: 'jquery',
				'window.jQuery': 'jquery'
			})
		]
	}
}

```



二、在vue-cli脚手架项目中使用bootstrap4框架的步骤
1、在main.js中引入bootstrap

npm i jquery bootstrap@4.6 popper.js -S
1
2、在main.js中引入bootstrap

```js
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap/dist/js/bootstrap.js'  
```

​     

3、在项目的根目录新建一个配置文件vue.config.js,输入以下代码

```js
const webpack = require("webpack")
module.exports = {
	// 配置插件参数
	configureWebpack: {
		plugins: [
			// 配置 jQuery 插件的参数
			new webpack.ProvidePlugin({
                // 引入jquery
				$: 'jquery',
				jQuery: 'jquery',
				'window.jQuery': 'jquery',
                // 引入popper.js
				Popper: ['popper.js', 'default']
			})
		]
	}
}
```





版权声明：本文为CSDN博主「乐sophie」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/qq_39784865/article/details/117653283