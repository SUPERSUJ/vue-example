# v-if

```
<div id="app">
  <h2 v-if="isShow">isShow</h2>
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    data() {
      return {
        isShow: false,
      };
    },
  });
</script>
```

```
compiled = {
  ast: {
    attrs: [{name: "id", value: ""app""}],
    attrsList: [{name: "id", value: "app"}],
    attrsMap: {id: "app"}
    children: [{
      attrsList: []
      attrsMap: {v-if: "isShow"}
      children: [{
        static: true
        text: "isShow"
        type: 3
      }]
      length: 1
      if: "isShow"
      ifProcessed: true
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: true
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
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[(isShow)?_h('h2',["isShow"]):_e()])}"
  staticRenderFns: []  
}
```