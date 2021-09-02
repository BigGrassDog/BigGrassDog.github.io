---
title: 关于hexo
date: 2021-08-26 14:41:43
tags: 'hexo'
---

# 常用命令

- 安装 git 部署插件

```[node]
npm i --save hexo-deployer-git
```

- 清理当前静态文件

```[node]
hexo clean
```

- 新建文章

```[node]
hexo new post "article title"
```

- 生成静态文件

```[node]
hexo g
```

- 启动本地博客服务

```[node]
hexo s
```

- 发布至 github 仓库

```[node]
  hexo d
```

# 连接 github 与本地

- 在 git bash 中根据注册 github 的信息设置用户名和邮箱

```[git]
  git config --global user.name '<username>'
  git config --global user.email '<user email>'
```

- 生成密钥 SSH key

```
ssh-keygen -t rsa -C 'user email'
```

_打开 <font color=SkyBlue>github</font>，在头像下面点击 <font color=SkyBlue>settings</font>， 再点击 <font color=SkyBlue>SSH and GPG keys</font>，新建一个 SSH。_

- 输出密钥 并复制 添加至 <font color=SkyBlue>github</font>

```
cat ~/.ssh/id_rsa.pub
```

- 验证是否连接成功

```
ssh -T git@github.com
```

# 修改配置

- 打开 <font color=red>\_config.yml</font> 配置文件

```[node]
deploy:
  type: 'git'
  repo: 'https://github.com/DogGrass/DogGrass.github.io'
  branch: 'master'
  message: 'grassdog_blog'

```
