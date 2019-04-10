<template>
  <div class="page">
    <ul @click="pageClick(1)" v-for="page in pages" :key="page.index">
      <li><a href="javaScrip(void)">首页</a></li>
      <li v-if="state = 1"><a href="javaScrip(void)">上一页</a></li>
      <li><a href="javaScrip(void)">1</a></li>
      <li><a href="javaScrip(void)">2</a></li>
      <li><a href="javaScrip(void)">3</a></li>...
      <li v-if="state = 1"><a href="javaScrip(void)">下一页</a></li>
      <li><a href="javaScrip(void)">尾页</a></li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "page",
  data(){
      return{
      //一个页三个表单数组数据
      //pages需要计算出总多少页（总数据长度除3（但最后一页只有一个怎么处理）），当前页数状态（双向绑定，每次访问初始化,不能为负数）
      //要取（方法传入state+1，传出三个表单数据）第几页绑定的三个数据，填上数据
      
        pages: [
        {},
      ],
      //总页，单个页面数，当前状态
      pageSum: 9,
      pageNum: 3,
      pageState: 0,  
      }
  },
  methods: {
    pageClick:function(count){
      this.count += count;
    },
    pageSum:function(arrayNum){
      if(arrayNum <= 3) return;
      else return arrayNum/3;
    },
    pageNext:function(state){
      
    },
    
  },
  computed: {

  }
};
</script>
<style lang="scss" scoped>
ul li {
  text-align: center;
  display: inline;
  margin: 0;
  padding: 0;
  list-style: none;
}
/* 分页 */
.page {
  margin: 40px 20px 40px 0;
  float: right;
}
.page a{
  text-decoration: none;
  margin-right: 5px;
  padding: 8px 15px;
  line-height: 25px;
  border: 1px solid rgb(242, 242, 242);
  background-color: rgb(221, 230, 230);
}
.page a:hover {
  cursor: pointer;
  background-color: blue;
  color: white;
}
</style>

