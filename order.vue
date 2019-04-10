<template>
  <div class="order">
    <div class="navTop">
      <a href="javaScrip(void)">首页</a>
      <span>></span>
      <a href="javaScrip(void)">订单中心</a>
    </div>
    <div class="nav">
      <ul>
        <li>
          <a href="javaScrip(void)">
            <span class="orderCenter">
              <img src="../assets/orderCenter.png">
            </span>订单中心
          </a>
        </li>
        <li>
          <a href="javaScrip(void)">所有订单</a>
        </li>
        <li class="collectionLi">
          <a href="javaScrip(void)">
            <span class="collection">
              <img src="../assets/collection.png">
            </span>我的收藏
          </a>
        </li>
        <li>
          <a href="javaScrip(void)">
            <span class="set">
              <img src="../assets/set.png">
            </span>账号设置
          </a>
        </li>
        <li>
          <a href="javaScrip(void)">收货地址</a>
        </li>
        <li>
          <a href="javaScrip(void)">修改密码</a>
        </li>
      </ul>
    </div>
    <div class="context">
      <div class="contextTop">所有订单</div>
      <div class="orderMsg">
        <form action>
          <ul>
            <li>
              <span>订单中心</span>
              <input type="text">
            </li>
            <li>
              <span>订单日期</span>
              <input type="text">-
              <input type="text">
            </li>
            <li>
              <span>订单状态</span>
              <select name="state">
                <option value="complete">完成</option>
                <option value="unfinished">未完成</option>
              </select>
            </li>
          </ul>
          <button>查询</button>
        </form>
      </div>
      <div class="orderContext">
        <!-- 循环使用组件？ -->


        <orderContext ref="orderContext-1"></orderContext>
        <orderContext ref="orderContext-2"></orderContext>
        <orderContext ref="orderContext-3"></orderContext>
        <page></page>
      </div>
    </div>
  </div>
</template>

<script>
import orderContext from "./orderContext.vue";
import page from "./page.vue";
export default {
  name: "order",
  components: {
    orderContext,page
  },
  data() {
    return {
      count: 0
    };
  },
  methods: {},
  computed: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
h1,
h2,
ul {
  margin: 0;
  padding: 0;
}
ul li {
  text-align: center;
  margin: 0;
  padding: 0;
  list-style: none;
}
a {
  text-decoration: none;
}
/*order*/
.order {
  margin: 0 auto;
  padding: 15px 5%;
  background-color: rgb(242, 242, 242);
  overflow: hidden;
}
/*navTop*/
.navTop {
  margin-bottom: 15px;
}
/*nav*/
.nav {
  float: left;
  text-align: center;
  vertical-align: middle;
  width: 14%;
  padding: 40px 0;
  background-color: white;
}
.nav ul {
}
.nav li {
  position: relative;
  line-height: 30px;
  margin-bottom: 10px;
}
.orderCenter {
  position: absolute;
  left: 18%;
  top: 10%;
}
.collection {
  position: absolute;
  left: 10%;
  top: 13%;
}
.set {
  position: absolute;
  left: 18%;
  top: 10%;
}
li.collectionLi {
  margin: 20px;
}
/*context*/
.context {
  width: 84%;
  float: right;
  background-color: white;
}
.context li {
  display: inline-block;
}
.contextTop {
  padding: 10px 20px;
  border-bottom: 20px solid rgb(242, 242, 242);
  background-color: white;
}
/* .orderMsg */
.orderMsg {
  padding: 20px 40px;
  border: 20px solid white;
  background-color: rgb(242, 242, 242);
}
.orderMsg li {
  margin: 0 40px 20px 0;
  line-height: 30px;
}
.orderMsg input {
  margin: 0 10px;
  height: 22px;
}
.orderMsg select {
  width: 145px;
  height: 24px;
  margin: 0 10px;
}
.orderMsg button {
  padding: 5px 40px;
  margin-left: 83%;
  display: block;
  color: blue;
  border: 1px solid blue;
}
</style>
