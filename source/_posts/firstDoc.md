---
title: JS一个数组A是否全包含另一个数组B
date: 2017-10-25 23:01:36
tags: 随笔
---
正文：
	function isContained(a, b){
	    if(!(a instanceof Array) || !(b instanceof Array)) return false;
	    if(a.length < b.length) return false;
	    var aStr = a.toString();
	    for(var i = 0, len = b.length; i < len; i++){
	       if(aStr.indexOf(b[i]) == -1) return false;
	    }
	    return true;
	}