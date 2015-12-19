# 常用工具类 utils.js #

## cookie ##

用于读取/写入/删除浏览器 `cookie`。使用方法：    
读取：`Utils.cookie('name');`    
写入：`Utils.cookie('name', 'zhuyujia'); 或者 Utils.cookie('age', 28, {expires: 1});`    
删除：`Utils.cookie('name', null);`

## addFavorite ##

添加到收藏夹，使用方法：`Utils.addFavorite(obj, {'title': 'your_title', 'url': 'your_url'});`

## fontSizeChange ##

改变文本字体大小，使用方法：`Utils.fontSizeChange({'range': 1, 'min': 14, 'max': 20, 'disabledClass': 'disabled', 'btnLargeId': 'large', 'btnSmallId': 'small', 'target': 'wrapper'});`

## placeholder ##

输入框占位符提示语，支持 `input` 和 `textarea`，使用方法：`Utils.placeholder('name', '请输入', 'tip');`

## setHome ##

设置为首页，使用方法：`<a href="javascript:;" onclick="Utils.setHome(this, window.location.href);">设为首页</a>`