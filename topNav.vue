<template>
  <div class="topNav">
    <div>
       首页<span>></span>订单中心
    </div>
    <div class="nav">
        <ul>
            <li>订单中心</li>
            <li>我的收藏</li>
            <li>账户设置</li>
        </ul>
    </div>
    <div class="context">

    </div>
    </div>
</template>

<script>
export default {
  name: 'topNav',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>


<style scoped>
.topNav{
    margin: 0 auto;
    width: 90%;
    background-color: whitesmoke;
}
.nav{
    width: 25%;
    background-color: #fff;

}
.context{
    width: 60%;
}
h1, h2 {
  margin: 0;
  padding: 0;
}


</style>
