git push -u origin master之后出现：



```csharp
Everything up-to-date
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

在这里，git提交改动到缓存，要push的时候不会将本地所有的分支都push掉，所以需要将分支的改动提交，然后合并分支。

1、确认是否处于分支中



```undefined
E:\code\ssc\10_mobile\ssc_app>git branch
 *  dev
master
```

如果没有分支，要先创建分支



```undefined
git branch dev
```

2、提交改动到分支



```csharp
gti add .
git commit -m '修改'
```

3、将新分支提交的改动合并到主分支上



```undefined
git merge dev
```

4、提交



```undefined
git push -u origin master
git checkout dev
```



作者：swluan
链接：https://www.jianshu.com/p/26f4dcfaea8e
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。