<body>
<template>
    <div id="post-a">
      <componentA title="Hello World"></componentA>

    </div>
  <div id="app">
    <globalComponent>{{name}}</globalComponent>
  </div>
</template>

<script>
  import Vue from 'vue';
  import Vue from 'vue';
  const app = Vue.createApp({})

  app.component('globalComponent', {


  })


  app.mount('#app')
  // const a=Vue.createApp({})
  // a.component('componentA',{
  // props:['title'],
  // template: `<h4>{{title}}</h4>`
  // })
  // // a.mount('#post-a')
  // // export default {
  // //   name: 'postVue'
  // // }
  // new Vue({ el: '#post-a' })

</script>
</body>
