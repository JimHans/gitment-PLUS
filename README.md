# Gitment-CN
#### Gitment评论框中文汉化版本，从提醒到UI完全汉化（错误信息未汉化以便查找错误）
# 使用方法：
### 第一步: 注册 OAuth Application
在 GitHub 上注册一个新的 OAuth Application。前面3项内容都可以随意填写，但要确保最后一个 Authorization callback URL 是你的网站域名(比如http://www.leyoblog.top)。
成功注册之后，你将会得到一个 client ID 和一个 client secret，这个将被用于之后的实例化 Gitment。

### 第二步: 页面引入 Gitment 的静态资源文件
```html
<link rel="stylesheet" href="https://raw.githubusercontent.com/JimHans/gitment-CN/master/gitment.css">
<script src="https://raw.githubusercontent.com/JimHans/gitment-CN/master/gitment.js"></script>
```
### 第三步: 部署 Gitment
在你要添加Gitment的页面位置添加以下代码
 ```javascript
 <div id="container"></div>
<script>
var gitment = new Gitment({  
  id: '页面 ID', // 可选。默认为 location.href  
  owner: '你的 GitHub Name',              
  repo: '存储评论的 repo',                  
  oauth: {    
  client_id: '你的 client ID',            
  client_secret: '你的 client secret',  
  },})gitment.render('container')</script>
```
注意：
##### 1.gitment.render()这个方法的参数就是你的评论区域 div 的 id 名;
##### 2.页面 ID 如果不写，默认为 location.href。


