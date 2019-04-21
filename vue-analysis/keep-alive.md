> keys 

```
var componentOptions = vnode && vnode.componentOptions;
var key = vnode.key == null
    // same constructor may get registered as different local components
    // so cid alone is not enough (#3269)
    ? componentOptions.Ctor.cid + (componentOptions.tag ? ("::" + (componentOptions.tag)) : '')
    : vnode.key;
```

> 清除缓存

```
function pruneCacheEntry (
  cache,
  key,
  keys,
  current
) {
  var cached = cache[key];
  if (cached && (!current || cached.tag !== current.tag)) {
    cached.componentInstance.$destroy();
  }
  cache[key] = null;
  remove(keys, key);
}
```

> 获取组件的name

```
// opts 就是vnode的componentOptions
function getComponentName (opts) {
  return opts && (opts.Ctor.options.name || opts.tag)
}
```

```
$0.__vue__.$options.__proto__.name
$.__vue__.$options.name
```

> 获取父组件keep-alive实例

```
$0.__vue__.$vnode.parent.componentInstance
```