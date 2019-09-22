<template>
  <div class="load-keeper  d-flex justify-content-center align-items-center" >

      <div v-if="!isLoad" class="spinner-border ms  text-success" style="width: 3rem; height: 3rem;" role="status">
  <span class="sr-only">Loading...</span>
</div>
 <img @load="loadImg"
  src='https://image.opeqe.com/gallery/small/23.jpg' 
  class="w-100 h-100" >
  </div>
</template>

<script>
export default {
    data(){
        return{
            isLoad:false
        };
    },
methods:{
    loadImg(e){
        console.log(e)
        console.dir(e)
        this.isLoad=true
        console.log(this.isLoad)
    //     if (this.$el.querySelector('img').readyState == "complete") { 
    //     // run code here
    //     console.log('loads')
    // } 
    }
}

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.load-keeper{
    position: relative;
    height: 20vh;
    .ms{
    position: absolute;
    
    // transform: translate(-50%,-50%)
    }
}
</style>
