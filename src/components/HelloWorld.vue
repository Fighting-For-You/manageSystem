<template>
  <div style="height: 100%;width: 100%;">
    <!-- <p><router-link to="/select">筛选</router-link></p>
				<p><router-link to="/treeTable">1.树状权限表格</router-link></p>
        <p><router-link to="/dragDropTree">2.拖拽树</router-link></p>-->
    <!-- <p>{{fn1()}}</p>
        <child-a></child-a>
        <button @click="changeUrl()">11111111111111</button>-->
    <!-- <child-a :a='msg'> </child-a> -->
    <!-- <router-link to="/aaa">a</router-link>
        <router-link to="/bbb">b</router-link>
        <router-link to="/ccc">c</router-link>
        <router-link to="/ddd">d</router-link>

         <router-view></router-view> -->
    <ul>
      <router-link to="/"
                   tag="li"><a>首页</a></router-link>
    </ul>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data () {
    return {
      //  msg: '我是父组件的数据'
    };
  },
  components: {     
    // 'child-a':{
    //   template:'<div>我是childa组件--{{a}}</div>',
    //   props:['a'],
    //   data(){
    //     return {
    //       num:100
    //     } 
    //   }
    // }
    "home": {
      template: '<div>aaa</div>'
    },
    routes: [
      { name: 'home', path: '/home', component: 'home ' }
    ]
  },
  methods: {
    fn1 () {
      console.log(111);
      return new Date();
    },
    changeUrl () {
      //
      this.$router.push({
        path: "treeTable"
      });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
