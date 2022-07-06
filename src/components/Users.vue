
<template>
  <div id="users">
    <h1>用户信息添加</h1>
    <form v-on:submit="addUser">
      用户名：<input type="text" v-model="newUser.name">
      用户年龄：<input type="text" v-model="newUser.age">

      <input type="submit" value="提交">
    </form>

    <ul>
      <li v-for="(user) in users" :key="user">
        {{user.name}} :{{user.age}}
        <button v-on:click="deleteUser(user)">删除</button>
      </li>
    </ul>
  </div>

</template>

<script src="src/js/vue.js">

export default {
  name: 'userVue',
  data(){
    return{
      newUser:{},
      users:[
        {name:"张三",
          age:"18"
        },
        {name:"李四",
          age:"16"
        },
        {name:"王五",
          age:"20"
        },
        {name:"张飞",
        age: "35"
        },
      ]
    }
  },
  methods:{
    addUser:function(e){
      //console.log("helloworld");
      this.users.push({
        name:this.newUser.name,
        age:this.newUser.age
      });
      console.log(e.preventDefault())
      e.preventDefault();
    },
    deleteUser:function(user){
      this.users.splice(this.users.indexOf(user),1);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>