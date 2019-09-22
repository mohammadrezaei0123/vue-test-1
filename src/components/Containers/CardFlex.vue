<template>
  <div class="container-fluid m-0 p-0">
      <div class="row d-flex justify-content-between w-100">
        <!-- <div class="d-flex align-items-between"> -->
          <button @click="back">l</button>
          <button @click="forward">f</button>
        <!-- </div> -->
      </div>
      <div class="row no-gutters">
          <div v-for="ix in total" :key="ix" class="col">
           <div>{{ix-1}} <Card v-if="checkpos(ix-1)"></Card></div>
            </div>
          <!-- <div class="col"><Card></Card></div>
          <div class="col"><Card></Card></div>
          <div class="col"><Card></Card></div> -->
      </div>
  </div>
</template>

<script>
import Card from "../Cards/ColCard";
export default {
  mounted(){
    this.resize()
    window.addEventListener("resize",this.resize)
  },
  methods:{
    back(){
      let inside=this.postion-this.num
      if(inside<0){
        if(this.postion==0){
          this.postion=this.total-this.num
        }else{
          this.postion=0
        }
      }else{
        this.postion=inside
      }
    },
    forward(){
      let outside=this.postion+this.num
      if(outside>=this.total){
        this.postion=0
      }else{
        this.postion=outside
      }
    },
    resize () {
      console.log("resize",this.num)
      let winWidth=window.innerWidth;
      // console.log(winWidth)
      if(winWidth<540){
        this.num=1
      }else if(winWidth<720){
        this.num=1
      }else if(winWidth<960){
        this.num=2
      }else{
        this.num=3
      }
      console.log(this.num)
    },
    checkpos(ix){
      // console.log(object)
      return ((this.postion+this.num)>ix && ix>=this.postion)
    }
  },
  data(){
    return{
      postion:0,
      num:4,
      total:10
    }
  },
components:{
Card
}
}
</script>

<style lang="sass" scoped>

</style>