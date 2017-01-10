# Zepto Autocomplete Plugin
根据https://github.com/Stayzilla/zepto-autocomplete插件修改，添加隐藏域传值，解决与SUI Mobile框架的冲突
#Examples

## 在引用插件之后，需要添加两个class（`autocomplete-input` and `autocomplete-result`）分别作为input输入框及显示区域.

<input type="text" class="autocomplete-input">
<div class="autocomplete-result"></div>

## 初始化加载options参数信息.
## 以下例子为数据本地化

    $(document).ready(function () {
      var autocompleteData = ["madras","london", "paris", "stockholm", "delhi", "madrid", "madurai"];
      var localOptions = {limit: 2, datasource: 'local', data: autocompleteData};
      $.fn.autocomplete(localOptions);
      ...
      ...
    }

## 远程加载数据

    $(document).ready(function () {
      var remoteOptions = {limit: 2, datasource: 'remote', data: 'example.json?keyword='};
      $.fn.autocomplete(remoteOptions);
      ...
      ...
    }

## Set caseSensitive to false to enable case-insensitive matching
## Leave this option off to use the default case-sensitive matching

    $(document).ready(function () {
      var remoteOptions = {limit: 2, datasource: 'remote', data: 'example.json?keyword=', caseSensitive: false};
      $.fn.autocomplete(remoteOptions);
      ...
      ...
    }

## 设置'show' and 'hide' options 如果你想要隐藏或者显示 如果你想要重写默认值，可以使用 $.show() and $.hide() 操作 

    var options = {
      limit: 2, 
      datasource: 'remote', 
      data: 'example.json?keyword=', 
      show: function(){ ... },
      hide: function(){ ... }
    };
    
## 设置隐藏域 ,options中的id为隐藏域id值，无特殊情况此方法一般用不到
    var options = {
      limit: 2, 
      datasource: 'remote', 
      id:'id',
      data: 'example.json?keyword=', 
      show: function(){ ... },
      hide: function(){ ... }
    };
    
## 如有不足,欢迎大家指导

License

Copyright (c) 2017 http://chenghaifeng.com/ Licensed under the MIT license.
