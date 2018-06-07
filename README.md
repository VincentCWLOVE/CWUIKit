# CWUIKit

> 在Vue中构建项目需求的组件

在Vue中构建组件的方式：

1. 使用`template`

```JavaScript
// 全局注册
Vue.component('my-component-name',{
    data: function() {
        return {
            pro1:1
        }
    },
    props:{
        
    },
    template:'<div></div>'
})

// 局部注册

let my-component-a = {
    data: function() {
        return {
            pro1:1
        }
    },
    props:{
        
    },
    template:'<div></div>'    
}

let my-component-b = {
    data: function() {
        return {
            pro1:1
        }
    },
    props:{
        
    },
    template:'<div></div>'    
}
let my-component-c = {
    data: function() {
        return {
            pro1:1
        }
    },
    props:{
        
    },
    template:'<div></div>'    
}


new Vue({
    el:"#app",
    components:[
        my-component-a,
        my-component-b,
        my-component-c
    ]
})

```

2. 使用 `render`函数

```javacript
export default {
    name:"CWUIView",

    componentName:'CWUIView',

    props:{

    },

    render(h){

        return h('div',{
            class:{
                'cwuiview':true
            },
            style:this.style,
            // attrs
            attrs: {
                name1:"Vincent",
                name2:"CW"

            },
            //DOM属性
            domProps:{
                // innerHTML:"vincent",
                // innerText:"love"

            },
            // props
            props: {

            },
            // 事件监听
            on: {

            }
        },this.$slots.default)
    }

}
```