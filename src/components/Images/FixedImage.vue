<template>
  <div 
      :style="setHeight"
  class="img ">
      <!-- <img 
       class="w-100" src="../../assets/images/p (1).jpg"> -->
  </div>
</template>

<script>
export default {
props:{
    imgHeight:Number
},
mounted(){
    let imgSize=100
    let self= this.$el
    setTimeout(function () {
      let  inter=setInterval(function () {
            imgSize+=0.1
            // console.log(self.$el.style)
            self.style.backgroundSize=imgSize+"% "+imgSize+"%";
            if(imgSize>=200){
                clearInterval(inter)
            }
       },5)
    },500)
},
computed:{
    setHeight(){
        console.log(this.imgHeight)
        // if(this.imgHeight){
        //     this.imgHeight=20
        // }
        return `height: ${this.imgHeight}vh;`
    }
},
beforeDestroy(){
//   window.removeEventListener("resize",this.resizeInput)
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
    height: 40vh;
    background-image: url('../../assets/images/p (1).jpg');
    background-position: center;
    background-attachment: fixed;
    background-size: 100% 100%;
}
</style>
