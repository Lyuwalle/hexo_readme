
hexo官方文档：
https://hexo.io/zh-cn/docs/

icarus主题官方文档：
https://ppoffice.github.io/hexo-theme-icarus/

# hexo个人博客步骤

## 1. 环境准备
安装Node.js
安装Git

## 2. 安装hexo
```
npm install -g hexo-cli
或者
cnpm install -g hexo-cli
```

初始化hexo，新建存储博客的文件夹
```
hexo init myblog
```

进入文件夹，安装一下npm
```
cd myblog
npm install
```

本地启动hexo
```
hexo g 
hexo server
```
访问http://localhost:4000/ 

## 3. github访问
新建仓库：用户名+.github.io

安装hexo上传插件
npm install hexo-deployer-git --save

修改hexo配置文件指定仓库路径
vim _config.yml 
#找到Deployment
```
# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
  type: git
  repo: https://github.com/Lyuwalle/Lyuwalle.github.io
  branch: master
```

推送站点到github
```
hexo d
```

稍等之后访问：lyuwalle.github.io

## 4. 修改主题为icarus
使用NPM将Icarus安装为Node包，在Hexo站点根目录运行如下命令：
```
npm install -S hexo-theme-icarus hexo-renderer-inferno
```

_config.yml文件中的开启Icarus：
```
theme: icarus
```

更新到github。后面添加文章时，也是使用这几个命令把文章上传到github
//清理
hexo clean
//构建静态文件
hexo g
//上传至仓库
hexo d

## 5. 写文章
根站点：
hexo new "我的第一篇博客"



