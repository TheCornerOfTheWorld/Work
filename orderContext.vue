<template>
  <div class="orderContext">
    <div class="orderContextborder">
      <div class="orderContextTop">
        <ul v-for="order in orders" :key="order.index">
          <li>
            <input type="checkbox">
            {{order.time}}
          </li>
          <li>订单号：{{order.num}}</li>
          <li>制作人：{{order.person}}</li>
        </ul>
      </div>
      <div class="orderContextTable">
        <table cellspacing="0" cellpadding="0">
          <tr>
            <th>商品</th>
            <th>单价</th>
            <th>数量</th>
            <th>总价</th>
            <th>备注</th>
            <th>状态</th>
            <th>操作</th>
          </tr>
          <tr v-for="orderGood in orderGoods" :key="orderGood.index">
            <td class="goods">
              <img :src="orderGood.src" alt="goods">
              <span>{{orderGood.message}}</span>
            </td>
            <td>¥{{orderGood.price}}</td>
            <td>x{{orderGood.num}}</td>
            <td>¥{{orderGood.sum()}}</td>
            <td>{{orderGood.context}}</td>
            <td>{{orderGood.state}}</td>
            <td>
              <span>
                <a href="javaScrip(void)">查看详情</a>
              </span>
              <span>
                <a href="javaScrip(void)">再次购买</a>
              </span>
            </td>
          </tr>
        </table>
      </div>
    </div>
  </div>
</template>
<script>
import goods from "../assets/goods.png";
export default {
  name: "orderContext",
  props: {},
  data() {
    return {
      price: 0,
      num: 0,
      orders: [{ time: "2019-09-09", num: 123, person: "李帅" }],
      orderGoods: [
        {
          // 可以把它放static或者是导入到其中
          src: goods,
          message:
            "得力(deli)22215 PU材质25k商务绑带皮面本/记事本/日记本 可插笔",
          price: 16.8,
          num: 10,
          sum: function() {
            return this.price * this.num;
          },
          context: "无",
          state: "已完成"
        }
      ]
    };
  }
};
</script>
<style scoped>
ul li {
  text-align: center;
  display: inline;
  margin: 0;
  padding: 0;
  list-style: none;
}
/* .orderContext */
.orderContext {
  margin-bottom: 20px;
  padding: 0 20px;
  background-color: white;
}
.orderContextborder {
  border: 2px solid rgb(242, 242, 242);
}
.orderContextTop {
  margin: 15px 20px;
}
.orderContextTop li {
  margin-right: 60px;
}
.orderContextTop input {
  margin-right: 10px;
}
/* 表格 */
.orderContextTable table {
  width: 100%;
  text-align: center;
}
.orderContextTable th {
  height: 40px;
  background-color: rgb(242, 242, 242);
}
.orderContextTable td {
  border-top: 3px solid blue;
  padding: 20px 0;
}
.orderContextTable a {
  display: block;
}
.goods {
  width: 35%;
}
.goods img {
  float: left;
}
.goods span {
  display: inline-block;
  width: 71%;
  margin: 20px 0px;
}
.orderContextTable {
  text-align: center;
}
</style>
