# v-html

```
<div id="app">
  <div v-html="html"></div>
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    data() {
      return {
        html: '<h1>hello</h1>',
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
      attrsList: [{name: "v-html", value: "html"}]
      attrsMap: {v-html: "html"}
      children: []
      directives: [{name: "html", value: "html", arg: undefined, modifiers: undefined}]
      hasBindings: true
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: false
      props: [{name: "innerHTML", value: "_s(html)"}]
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
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_h('div',{domProps:{"innerHTML":_s(html)}})])}"
  staticRenderFns: []
}
```