<template>
  
  <div>animation
      <transition name="bounce">
      <div v-if="show" >
      fffffffffffffffff
      ffffffff
  </div>
  </transition>
  </div>
</template>

<script>
export default {
    mounted(){
        document.addEventListener("scroll",this.scroll)
    },
    beforeDestroy(){
        document.removeEventListener("scroll",this.scroll)
    },
data(){
    return{
        show:false
    }
},methods:{
        scroll () {
            var doc = document.documentElement;
            var lefta = (window.pageXOffset || doc.scrollLeft) - (doc.clientLeft || 0);
            var top = (window.pageYOffset || doc.scrollTop)  - (doc.clientTop || 0);
            // var rect = this.$el.getBoundingClientRect();
            // console.log(rect.top, rect.right, rect.bottom, rect.left);
            // console.log(top,' ',lefta)
            // console.log(document.documentElement.scrollTop)
            // console.log("el")
            // console.log(this.$el.offsetTop)
            // console.log((this.$el.offsetTop+window.innerHeight))
            // console.dir(this.$el)
            if(top>=(this.$el.offsetTop-window.innerHeight+250)){
                // console.log(top," ",rect.top)
                this.$el.style.backgroundColor='red'
                this.show=true
                // console.log('yes')
            }else{
                
                this.$el.style.backgroundColor='blue'
                this.show=false
            }
            // if(top>=25){
            //     this.$el.style.boxShadow=" 0px 3.2px 5px grey";
            // }else{
            //     this.$el.style.boxShadow="none";
            // }
        }
    }
}
</script>

<style scoped>
div{
  overflow: hidden;
  overflow-x: hidden;
}
.bounce-enter-active {
  animation: bounce-in 2s;
  /* transform: () */
}
.bounce-leave-active {
  animation: bounce-in 2s reverse;
}
@keyframes bounce-in {
  0% {
    transform: translateX(-100%);
  }
  /* 50% {
    transform: scale(1.5);
  } */
  100% {
    transform: translateX(0);
  }
}

/* .fade-enter-active, .fade-leave-active {
  transition: opacity 1s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
} */
</style>