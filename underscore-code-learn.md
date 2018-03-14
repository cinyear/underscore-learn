### 对集合类

```javascript

// 数组最大长度
var Max_ARRAY_INDEX = (Math.pow(2, 53)) - 1;
// 获取长度
var getLength = property("length")
// 判断是否是类数组对象
var isArrayLike = function (collection) {
    var length = getLength(collection)
    return (((typeof length == "number") && (length >= 0)) && (length <= MAX_ARRAY_INDEX))
}

_.each = _.forEach = function (obj, iteratee, context) {
    // 将执行函数与上下文绑定 返回新回调函数
    iteratee = optimizeCb(iteratee, context)
    
    // 对类数组 进行遍历  类似数组的遍历
    
    // 对非类数组的遍历  iteratee(属性值， 属性， 对象)
    
    // 返回 iteratee 操作后的 obj
    return obj
}

_.map = _.collect = function (obj, iteratee, context) {
    // 返回新函数
    iteratee = cb(iteratee, context)
    // keys 判断非数组 获取属性数组
    var keys = (!(isArrayLike(obj))) && (_.keys(obj)),
        // 此处有疑问--> length = (keys || obj).length
        // 获取 对象属性数组的长度  或者类数组、数组的长度
        length = （keys || obj）.length,
        // 创建空数组 长度与属性值、类数组、数组 长度一致
        results = Array(length);
    // 对属性进行循环  对类数组、数组进行循环
    // 将属性值 属性 对象本身 / 数组项 索引 （类）数组本身  通过 iteratee 执行后 结果放入 results
    for(var index = 0; index < length; index++) {
        
    }
}
```

