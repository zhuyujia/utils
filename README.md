# 常用工具类 zUtils.js #

## cookie ##

用于读取/写入/删除浏览器 cookie。使用方法：  
读取：`zUtils.cookie('name');`  
写入：`zUtils.cookie('name', 'zhuyujia');` 或者 `zUtils.cookie('age', 28, {expires: 1});`  
删除：`zUtils.cookie('name', null);`  
@param  {String} name  读取/写入/删除 cookie 的名称  
@param  {String} value 需要设置 cookie 的值  
@param  {Object} opts  其他参数，有效期 expires 单位小时，路径 path，域名 domain，安全性 secure  
@return {String}       有 cookie 就返回 cookie 的值，没有返回 null

## addFavorite ##

添加到收藏夹，使用方法：`<a href="javascript:;" onclick="zUtils.addFavorite(this)">点击收藏</a>`  
@param {Object} obj  指代触发函数的上下文，一般用 this  
@param {Object} opts 收藏夹的标题和链接，默认为当前页面的标题和链接 {title: 'your_title', url: 'your_url'}

## fontSizeChange ##

改变文本字体大小，使用方法：`zUtils.fontSizeChange({'range': 1, 'min': 14, 'max': 20, 'disabledClass': 'disabled', 'btnLargeId': 'large', 'btnSmallId': 'small', 'target': 'wrapper'});`  
@param  {Object} opts 参数集合，参数如下：  
range：字体大小增加幅度，默认 1  
min：字体最小值，默认 12  
max：字体最大值，默认 20  
disabledClass：禁用样式名，默认 'disabled'  
btnLargeId：增大字体按钮的 id  
btnSmallId：减小字体按钮的 id  
target：字体改变的容器的 id

## placeholder ##

输入框占位符提示语，支持 `input` 和 `textarea` 标签，使用方法：`zUtils.placeholder('name', '请输入');`  
由于 placeholder 在 ie 浏览器中效果不理想，比如 ie6-9 不支持 placeholder，ie10 鼠标聚焦后文本消失，所以在 ie 浏览器中使用 label 标签模拟。  
@param  {String} id        文本输入框 id  
@param  {String} msg       占位符提示语文字  
@param  {String} className ie 浏览器占位符样式，默认 placeholder-tip

## setHome ##

设置为首页，使用方法：`<a href="javascript:;" onclick="zUtils.setHome(this, window.location.href);">设为首页</a>`  
@param {Object} obj 指代触发函数的上下文，一般用 this  
@param {String} url 设置为首页的地址

## getUrlParam ##

获取 url 后的参数，使用方法：`zUtils.getUrlParam('name');`  
@param  {String} name 参数名称  
@return {String}      有参数返回参数的值，没有返回 null