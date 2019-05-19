<template>
  <div id="app">
   <div class="title">
            <span v-for="(item,index) in list" :key="index">{{item.tab}}</span>
        </div>
        <div class="inner">
          <myList></myList>
        </div>
  </div>
</template>

<script>
import myList from './components/list'
export default {
  name: 'App',
  data(){
    return {
      list:[{
        tab:'综合',
        inn:[{
              img:'https://img01.hua.com/uploadpic/newpic/9012009.jpg',
              name:'忘情巴黎',
              Introduction:'33枝红玫瑰',
              Sales:'7.5万',
              NowPromo:'浪漫唯美 女神挚爱'
        }]
      },{
        tab:'销量',
        inn:[{
              img:'https://img01.hua.com/uploadpic/newpic/9012009.jpg',
              name:'忘情巴黎',
              Introduction:'33枝红玫瑰',
              Sales:'7.5万',
              NowPromo:'浪漫唯美 女神挚爱'
          },{
              img:'https://img01.hua.com/uploadpic/newpic/9010947.jpg',
              name:'真爱如初',
              Introduction:'雪山玫瑰11枝、深紫色勿忘我0.3扎',
              Sales:'6.9万',
              NowPromo:'已优惠30元'
          }]
      },{
        tab:'价格',
         inn:[{
              img:'https://img01.hua.com/uploadpic/newpic/9012009.jpg',
              name:'忘情巴黎',
              Introduction:'33枝红玫瑰',
              Sales:'7.5万',
              NowPromo:'浪漫唯美 女神挚爱'
          },{
              img:'https://img01.hua.com/uploadpic/newpic/9010947.jpg',
              name:'真爱如初',
              Introduction:'雪山玫瑰11枝、深紫色勿忘我0.3扎',
              Sales:'6.9万',
              NowPromo:'已优惠30元'
          },{
              img:'https://img01.hua.com/uploadpic/newpic/9092117.jpg',
              name:'忘情巴黎＋德芙心语巧克力98克特价组合套装',
              Introduction:'33枝红玫瑰',
              Sales:'5.5万',
              NowPromo:''
          }]
      },{
        tab:'最新',
        inn:[{
              img:'https://img01.hua.com/uploadpic/newpic/9012009.jpg',
              name:'忘情巴黎',
              Introduction:'33枝红玫瑰',
              Sales:'7.5万',
              NowPromo:'浪漫唯美 女神挚爱'
          },{
              img:'https://img01.hua.com/uploadpic/newpic/9010947.jpg',
              name:'真爱如初',
              Introduction:'雪山玫瑰11枝、深紫色勿忘我0.3扎',
              Sales:'6.9万',
              NowPromo:'已优惠30元'
          },{
              img:'https://img01.hua.com/uploadpic/newpic/9092117.jpg',
              name:'忘情巴黎＋德芙心语巧克力98克特价组合套装',
              Introduction:'33枝红玫瑰',
              Sales:'5.5万',
              NowPromo:''
          },{
              img:'https://img01.hua.com/uploadpic/newpic/9010011.jpg',
              name:'一心一意',
              Introduction:'玫瑰11枝，粉色勿忘我0.3扎',
              Sales:'7.7万',
              NowPromo:'已优惠10元'
          }]
      }]
    }
  },
  components: {
   myList
  }
}
</script>

<style>
    *{
      margin:0;
      padding: 0;
    }
    body,
    html,
    #app {
    width: 100%;
    height: 100%;
  }
  .title {
    display: flex;
    height: 50px;
    line-height: 50px;
    width: 100%;
  }
  .title span{
      flex: 1;
    text-align: center;
  }
</style>
