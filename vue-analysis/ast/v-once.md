# v-once

```
<div id="app">
  <span v-once>{{n}}</span>
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    data() {
      return {
        n: 1,
      };
    },
  });
</script>
```

```
compiled = {
  ast: {
    attrs: [{name: "id", value: ""app""}]
    attrsList [{name: "id", value: "app"}]
    attrsMap: {id: "app"}
    children: [{
      attrsList: []
      attrsMap: {v-once: ""}
      children: [{type: 2, expression: "_s(n)", text: "{{n}}", static: false}]
      once: true
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: true
      static: false
      staticInFor: false
      staticProcessed: true
      staticRoot: true
      tag: "span"
      type: 1
    }]
    parent: undefined
    plain: false
    static: false
    tag: "div"
    type: 1
  }
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_m(0)])}"
  staticRenderFns: ["with(this){return _h('span',[_s(n)])}"]
}
```