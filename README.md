# object-create-ie8
Object.create polyfill ie8

```javascript
if (!/\[native code\]/.test(Object.create)) {
    Object.create = function (a) {
        var f = function f() {};
        f.prototype = a;
        return new f();
    };
}

```
