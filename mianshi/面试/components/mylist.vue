<template>
  <div>
    <div class="tt">
      <h3>{{title}}</h3>
      <span>{{list[type]}}</span>
    </div>
    <p>{{content}}</p>
    <div class="time">
      <span>{{time}}</span><span>{{bool?'已提醒':'未提醒'}}</span>
    </div>
  </div>
</template>

<script>

export default {
  name:'mylist',
  props:['title','content','time','type','bool'],
  data(){
    return {
      list:['未开始','已完成','已放弃','全部']
    }
  },
  methods:{
      
  },
  components: {
   
  }
}
</script>

<style scoped>
p{
  padding:10px;
}
    .tt,.time{
      display: flex;
      justify-content: space-between;
      padding:10px;
      box-sizing: border-box;
    }
    
</style>


