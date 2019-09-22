<template>
  <div @click="goInput" class="parent-input bg-light">
      <img @click="goInput" class="h-100" src="../../assets/icons/ic_action_armchair.png">
      <input class="w-100 h-100 bg-info" placeholder="kkkkk"/>
  </div>
</template>

<script>
export default {
props:{

},
beforeDestroy(){
  // window.removeEventListener("resize",this.resizeInput)
},
mounted(){
  let widthImag=this.$el.querySelector('img').width;
  // window.addEventListener("resize",this.resizeInput)
  this.$el.querySelector('input').style.paddingLeft=widthImag+"px"
},methods:{
  goInput(){
    this.$el.querySelector('input').focus()
  },
  resizeInput(){
    console.log('this input resize')
  
  }
}

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
div{
    position: relative;
  img{
    position: absolute;
    left: 0
  }
}
</style>
