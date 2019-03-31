# v-text

```
<div id="app">
  <div v-text="txt"></div>
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    data() {
      return {
        txt: 'txt',
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
      attrsList: [{name: "v-text", value: "txt"}]
      attrsMap: {v-text: "txt"}
      children: []
      directives: [{name: "text", value: "txt", arg: undefined, modifiers: undefined}]
      hasBindings: true
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: false
      props: [{name: "textContent", value: "_s(txt)"}]
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
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_h('div',{domProps:{"textContent":_s(txt)}})])}"
  staticRenderFns: []
}
```