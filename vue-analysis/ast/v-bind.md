# v-bind

```
<div id="app">
  <img v-bind:src="src" />
</div>
<script src="../vue.2.0.1.js"></script>
<script>
  var vm = new Vue({
    el: '#app',
    data() {
      return {
        src: 'https://upload-images.jianshu.io/upload_images/6813214-e4ac9303963d05cc.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp',
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
      attrs: [{name: "src", value: "src"}]
      attrsList: [{name: "v-bind:src", value: "src"}]
      attrsMap: {v-bind:src: "src"}
      children: []
      hasBindings: true
      parent: {type: 1, tag: "div", attrsList: Array(1), attrsMap: {…}, parent: undefined, …}
      plain: false
      static: false
      tag: "img"
      type: 1
    }]
    parent: undefined
    plain: false
    static: false
    tag: "div"
    type: 1
  }
  render: "with(this){return _h('div',{attrs:{"id":"app"}},[_h('img',{attrs:{"src":src}})])}"
  staticRenderFns: []
}
```