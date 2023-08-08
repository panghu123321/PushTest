# 关于Git同时推送到多个平台

1. 创建多个空仓库

2. 创建项目

3. 初始化`Git`

   配置用户名和邮箱

   ```bash
   git config --global user.name '胖胖'
   git config --global user.email 'TigerRou@outlook.com'
   ```

   > 注：已配置的可跳过

​	  初始化仓库
   ```bash
   git init
   ```

​	配置推送仓库

```bash
git remote add github https://TigerRou@github.com/TigerRou/PushTest.git
git remote add gitee https://TigerRou@gitee.com/TigerRou/PushTest.git
git remote add gitlab https://TigerRou@git.sxs.icu/TigerRou/PushTest.git
```

> 按需配置代理

```bash
git config --global http.proxy http://127.0.0.1:7890
```



3. 提交文件

   ```bash
   git config --global core.auticrlf true
   git add .
   git commit -m '初始化项目'
   
   git push github
   git push gitee
   git push gitlab
   ```