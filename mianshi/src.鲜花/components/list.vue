<template>
  <div id="list">
    <div v-for="(item,index) in inn" :key="index" class="list">
        <div><img :src="item.img" alt=""></div>
                <div class="right">
                    <p>{{item.name}}</p>
                    <p>{{item.Introduction}}</p>
                    <p>{{item.Sales}}</p>
                    <p>{{item.NowPromo}}</p>
                </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'list',
  data(){
      return {
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
      }
  },
  methods:{
      
  },
  components: {
   
  }
}
</script>

<style>
    .list {
    display: flex;
    height: 200px;
    width: 100%;
}

.list  div {
    flex: 1;
}

.list  div img {
    height: 200px;
}

.right p {
    margin: 20px;
}
</style>


