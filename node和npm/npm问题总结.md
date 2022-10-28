# 清理缓存

```
npm cache clean --force
```







# npm版本问题报错

# npm ERR! code ERESOLVE npm ERR! ERESOLVE unable to resolve dependency tree

```bash
npm ERR! code ERESOLVE
npm ERR! ERESOLVE unable to resolve dependency tree
npm ERR! 
npm ERR! Found: webpack@5.11.1
npm ERR! node_modules/webpack
npm ERR!   dev webpack@"4.41.5" from the root project
npm ERR!   peer webpack@">=2" from babel-loader@8.2.2
npm ERR!   node_modules/babel-loader
npm ERR!     dev babel-loader@"^8.0.0" from the root project
npm ERR!   2 more (copy-webpack-plugin, css-loader)
npm ERR! 
npm ERR! Could not resolve dependency:
npm ERR! dev mini-css-extract-plugin@"^0.9.0" from the root project
npm ERR! 
npm ERR! Conflicting peer dependency: webpack@4.44.2
npm ERR! node_modules/webpack
npm ERR!   peer webpack@"^4.4.0" from mini-css-extract-plugin@0.9.0
npm ERR!   node_modules/mini-css-extract-plugin
npm ERR!
npm ERR! Fix the upstream dependency conflict, or retry
npm ERR! this command with --force, or --legacy-peer-deps
npm ERR! to accept an incorrect (and potentially broken) dependency resolution.
```

原因
ERESOLVE与npm@7有关的问题很常见，因为npm7.x对某些事情比npm6.x更严格。通常，最简单的解决方法是将--legacy-peer-deps标志传递给npm(e.g.，npm i --legacy-peer-deps），或者使用npm@6。

如果这不能立即起作用，也许可以先删除node_modules和package-lock.json。它们将被重新创建。

解决方案
降级npm到6版本

或

使用npx指定npm的版本

```npm
npm i --legacy-peer-deps
```



```bash
npx -p npm@6 npm i --legacy-peer-deps
```