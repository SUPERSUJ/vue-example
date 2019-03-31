# v-on

```
<div id="app">
  <div @click="open">点击</div>
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    methods: {
      open() {
        console.log(1);
      },
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
      attrsList: [{name: "@click", value: "open"}]
      attrsMap: {@click: "open"}
      children: [{type: 3, text: "点击", static: true}]
      events: {
        click: {value: "open", modifiers: undefined}
      }
      hasBindings: true
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: false
      static: false
      tag: "div"
      type: 1
    }]
    parent: undefined
    plain: false
    static: false
    tag: "div"
    type: 1
  }
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_h('div',{on:{"click":open}},["点击"])])}"
  staticRenderFns: []
}
```



```
<div id="app">
  <div @click="open(1)">点击</div>
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    methods: {
      open() {
        console.log(1);
      },
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
      attrsList: [{name: "@click", value: "open(1)"}]
      attrsMap: {@click: "open(1)"}
      children:[{type: 3, text: "点击", static: true}]
      events: {click: {value: "open(1)", modifiers: undefined}}
      hasBindings: true
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: false
      static: false
      tag: "div"
      type: 1
    }]
    parent: undefined
    plain: false
    static: false
    tag: "div"
    type: 1
  }
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_h('div',{on:{"click":function($event){open(1)}}},["点击"])])}"
  staticRenderFns: []
}
```