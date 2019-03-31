# v-show

```
<div id="app">
  <h2 v-show="isShow">isShow</h2>
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
    attrs: [{name: "id", value: ""app""}]
    attrsList: [{name: "id", value: "app"}]
    attrsMap: {id: "app"}
    children: [{
      attrsList: [{name: "v-show", value: "isShow"}]
      attrsMap: {v-show: "isShow"}
      children: [{
        static: true
        text: "isShow"
        type: 3
      }]
      directives: [
        arg: undefined
        modifiers: undefined
        name: "show"
        value: "isShow"
      ]
      hasBindings: true
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
    type: 1
  }
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_h('h2',{directives:[{name:"show",value:(isShow),expression:"isShow"}]},["isShow"])])}"
  staticRenderFns: []
}
```