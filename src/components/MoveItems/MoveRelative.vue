<template>
  <div class="content">
      <!-- <transition name="tester"> -->
          
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <RelativeShape :ph="setHeight" :pw="setWidth"/>
      <!-- </transition> -->
      <!-- <div class="shape" @loadstart="loads($event)"></div>
      <div class="shape" @loadstart="loads"></div>
      <div class="shape" @loadstart="loads"></div> -->
  </div>
</template>

<script>
import RelativeShape from "./RelativeShape";
export default {
    mounted(){
        // clg
        console.log("fffffffffffffsaf")
        console.dir(this.$el)
        console.log(this.$el,"  ddddddddd")
        this.h=this.$el.offsetHeight
        this.w=this.$el.offsetWidth
    },
    data(){
        return{
            w:500,
            h:500
        }
    },
    components:{
        RelativeShape
    },
computed:{
    setHeight(){
        console.log("s")
        console.dir(this.$el)
        return this.h
    },
    setWidth(){
        return this.w
    }
    // loads(){
    //     // console.log("fffffffffffffffffff")
    //     // console.log($event)
    //     // setInterval(this.changePos,500)
    // }
}
}
</script>

<style scoped>
/* .tester-enter-active,.tester-leave-active,.tester-enter,.tester-leave{
    transition:all 1s;
} */
.content{
    width: 100%;
    position: relative;
    height: 500px;
    background: aqua;
    /* transition:all 0.5s; */
    overflow: hidden;
    overflow-x: hidden;
    overflow-y: hidden;
}
.shape{
    position: absolute;
    top: 100px;
    width: 20px;
    height: 20px;
    background: red;
    border-radius: 50%;
}

</style>