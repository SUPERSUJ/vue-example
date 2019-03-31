# v-pre

```
<div id="app">
  <h2 v-pre>{{item}}</h2>
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
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