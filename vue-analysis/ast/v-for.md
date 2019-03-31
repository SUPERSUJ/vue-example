# v-for

```
<div id="app">
  <h2 v-for="(item, index) of arr" :key="index">{{item}}</h2>
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    data() {
      return {
        arr: [1, 2],
      };
    },
  });
</script>
```

```
compiled = {
  ast: {
    attrs: [{name: "id", value: ""app""}]
    attrsList: [{name: "id", value: "app"}]
    attrsMap: {id: "app"}
    children: [{
      alias: "item"
      attrsList: []
      attrsMap: {v-for: "(item, index) of arr", :key: "index"}
      children: [{
        expression: "_s(item)"
        static: false
        text: "{{item}}"
        type: 2
      }]
      for: "arr"
      forProcessed: true
      iterator1: "index"
      key: "index"
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: false
      static: false
      tag: "h2"
      type: 1
    }]
    parent: undefined
    plain: false
    static: false
    tag: "div"
    type: 1,
  }
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_l((arr),function(item,index){return _h('h2',{key:index},[_s(item)])})])}"
  staticRenderFns: []
}
```

```
<div id="app">
  <h2 v-for="(item, index) of arr" :key="index">{{item}}{{index}}</h2>
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    data() {
      return {
        arr: [1, 2],
      };
    },
  });
</script>
```

```
compiled = {
  ast: {
    attrs: [{name: "id", value: ""app""}]
    attrsList: [{name: "id", value: "app"}]
    attrsMap: {id: "app"}
    children: [{
      alias: "item"
      attrsList: []
      attrsMap: {v-for: "(item, index) of arr", :key: "index"}
      children: [{type: 2, expression: "_s(item)+_s(index)", text: "{{item}}{{index}}", static: false}]
      for: "arr"
      forProcessed: true
      iterator1: "index"
      key: "index"
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: false
      static: false
      tag: "h2"
      type: 1
    }]
    parent: undefined
    plain: false
    static: false
    tag: "div
  }
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_l((arr),function(item,index){return _h('h2',{key:index},[_s(item)+_s(index)])})])}"
  staticRenderFns: []
}
```


```
// render v-for
Vue.prototype._l = function renderList (
  val,
  render
) {
  var ret, i, l, keys, key;
  if (Array.isArray(val)) {
    ret = new Array(val.length);
    for (i = 0, l = val.length; i < l; i++) {
      ret[i] = render(val[i], i);
    }
  } else if (typeof val === 'number') {
    ret = new Array(val);
    for (i = 0; i < val; i++) {
      ret[i] = render(i + 1, i);
    }
  } else if (isObject(val)) {
    keys = Object.keys(val);
    ret = new Array(keys.length);
    for (i = 0, l = keys.length; i < l; i++) {
      key = keys[i];
      ret[i] = render(val[key], key, i);
    }
  }
  return ret
};
```