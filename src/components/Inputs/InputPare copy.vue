<template>
  <div class="d-flex ">
    
        <div @click="goInput" class="parent-input left flex-fill  bg-danger">
          <img @click="goInput" class="h-100 img" src="../../assets/icons/ic_action_armchair.png" />
          <input class="w-100 h-100 bg-danger" placeholder="kkkkk" />
        </div>
        <img @click="goInput" class="h-100 rounded-circle bg-warning center" src="../../assets/icons/ic_action_add.png" />
        <div @click="goInput" class="parent-input right flex-fill  bg-danger">
          <img @click="goInput" class="h-100 img" src="../../assets/icons/ic_action_armchair.png" />
          <input class="w-100 h-100 bg-danger" placeholder="kkkkk" />
        </div>
  </div>
</template>

<script>
export default {
  mounted(){
    let centerW=this.$el.querySelector('.center').width
    console.log(centerW)
    this.$el.querySelector('.left').style.marginLeft=-(centerW/2)+'px'
    console.log(this.$el.querySelector('.left').style.marginLeft)
    this.$el.querySelector('.right').style.marginRight=-(centerW/2)+'px'
    console.log(this.$el.querySelector('.right').style.marginRight)

  },
  methods:{
    goInput(){}
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
// .right{
//   padding-left: 50px
// }
// .left{
// padding-right: 50px;
// }
.center{
  position: absolute;
  top: 0;
  left: 50%;
  // margin-right: -50px;
  // margin-left:-50px;
  z-index:5
}
div {
  position: relative;
  .img {
    position: absolute;
    left: 0;
  }
}
</style>
