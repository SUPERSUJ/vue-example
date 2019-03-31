# v-model

```
<div id="app">
  <input type="text" v-model="val">
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    data() {
      return {
        val: '',
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
      attrs: [{name: "type", value: ""text""}]
      attrsList: [
        {name: "type", value: "text"}
        {name: "v-model", value: "val"}
      ]
      attrsMap: {
        type: "text"
        v-model: "val"
      }
      children: []
      directives: [{
        arg: undefined
        modifiers: undefined
        name: "model"
        value: "val"
      }]
      events: {
        input: {value: "if($event.target.composing)return;val=$event.target.value", modifiers: null},
      }
      hasBindings: true
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: false
      props: [{name: "value", value: "_s(val)"}]
      static: false
      tag: "input"
      type: 1
    }]
    parent: undefined
    plain: false
    static: false
    tag: "div"
    type: 1
  }
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_h('input',{directives:[{name:"model",value:(val),expression:"val"}],attrs:{"type":"text"},domProps:{"value":_s(val)},on:{"input":function($event){if($event.target.composing)return;val=$event.target.value}}})])}"
staticRenderFns: []
}
```