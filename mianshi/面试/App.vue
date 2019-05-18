<template>
  <div id="app">
   <div class="tab">
            <span v-for="(item,index) in typeList" 
            :key="index"
            @click="clicks(index)"
            :class="{'active':index==ind}"
            >{{item}}</span>
        </div>
       <div class="inner">
          <mylist 
          v-for="(item,index) in list" 
          :key="index"
          :title="item.title"
          :content="item.content"
          :type="item.type"
          :bool="item.bool"
          :time="item.time"
          >{{item}}</mylist>
          </div>
  </div>
</template>

<script>
import data from './mock'
import mylist from './components/mylist'
export default {
  components: {
   mylist
  },
  data(){
    return {
      ind:0,
      typeList:['未开始','已完成','已放弃','全部'],
      list:[],
    }
  },
  created(){
    console.log(data);
    this.data=data.list.filter(item=>item.type==1)
    console.log(this.list)
  },
 methods: {
   clicks(index) {
     this.ind = index;
      this.list=this.getList(index);
     },
   getList(type){
       return data.list.filter(item=>item.type==type)
     }
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
  .tab {
    display: flex;
    height: 50px;
    line-height: 50px;
    width: 100%;
  }
  .tab span{
      flex: 1;
    text-align: center;
  }
   .active {
            color: seagreen;
        }
        ul li{
          height: 50px;
          line-height: 50px;
          margin:20px;
          list-style: none;
        }
</style>
