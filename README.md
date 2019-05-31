# testJavaScript
测试套路

```javascript
// ======
// 测试
// ======
//
// 定义我们用于测试的函数
// ensure 接受两个参数
// condition 是 bool, 如果为 false, 则输出 message
// 否则, 不做任何处理
var ensure = function(condition, message) {
    // 在条件不成立的时候, 输出 message
    if(!condition) {
        log('*** 测试失败:', message)
    }
}
//升级版本
var ensureEqual = function(a,b, message) {
    // 在条件不成立的时候, 输出 message
    // 条件成立不输出
    if(a != b) {
        log(message,a,b)
    }
}
//例子
  /*
    s1 s2 都是 string
    但 s2 的长度是 1 
    返回 s2 在 s1 中的下标, 从 0 开始, 如果不存在则返回 -1
    */
 var find = function(s1,s2) {
    var index = -1;
    for(var i = 0; i < s1.length; i++) {
        if(s1[i] == s2){
            index = i;
            break;
        }
    }
     return index;
 }
 var ensure = function(condition, message) {
    // 在条件不成立的时候, 输出 message
    if(!condition) {
        console.log('*** 测试失败:', message)
    }
 }

var ensureEqual = function(a,b, message) {
    // 在条件不成立的时候, 输出 message
    if(a != b) {
        console.log(message,a,b);
    }
}

var text_find = function() {
    ensure(find("12345a","a") == "5",'"12345a"，"a",下标不是4');
    ensureEqual(find("12345a","a"),"5", '"12345a"，"a",下标不是5');

}


```
