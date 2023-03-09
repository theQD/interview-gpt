<template>
    <div>
        <button :on-click="make()">创建</button>
        <button :on-click="check()">查询</button>
        <div>{{a}}</div>
    </div>
    
</template>

<script>
export default {
  data(){
    return{
      a:2
    };
  },
  methods:{
    make(){
      this.whereJson = 1;
    },


  }
        
};
</script>


<style lang="scss" scoped>

</style>