<template>
  <div class="d-flex justify-content-center align-items-center mains">
    
        <div @click="goInput" class="parent-input left bg-transparent">
          <img @click="goInput" class="h-100 img" src="../../assets/icons/ic_action_armchair.png" />
          <input class="w-100 h-100 bg-transparent" placeholder="kkkkk" />
        </div>
        <img @click="goInput" class="rounded-circle bg-warning center" src="../../assets/icons/ic_action_add.png" />
        <div @click="goInput" class="parent-input right  bg-transparent">
          <img @click="goInput" class="h-100 img" src="../../assets/icons/ic_action_armchair.png" />
          <input class="w-100 h-100 bg-transparent" placeholder="kkkkk" />
        </div>
  </div>
</template>

<script>
export default {
  mounted(){
    
    this.$el.querySelector('.center').style.height=(this.$el.querySelector('.right').offsetHeight-5)+"px"
    let centerW=this.$el.querySelector('.center').offsetWidth 

    
    
    this.$el.querySelector('.right').style.marginLeft=-(centerW/2)+'px'
    this.$el.querySelector('.right img').style.left=(centerW/2)+'px'
    let rightImageW=this.$el.querySelector('.right img').offsetWidth
    this.$el.querySelector('.right input').style.paddingLeft=((centerW/2)+rightImageW)+'px'

    let leftImageW=this.$el.querySelector('.left img').offsetWidth
    this.$el.querySelector('.left').style.marginRight=-(centerW/2)+'px'
    this.$el.querySelector('.left input').style.paddingLeft=leftImageW+'px'
    this.$el.querySelector('.left input').style.paddingRight=(centerW/2)+'px'


  },
  methods:{
    goInput(){}
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.right{
  border-left: 1px solid beige;
}
.mains{
  width: fit-content;
  border: 1px solid beige;
}
input{
  outline: none;
  border: none;
}
.center{
  cursor: pointer;
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
