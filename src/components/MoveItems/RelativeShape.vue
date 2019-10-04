<template>
  <div></div>
</template>

<script>
export default {
    props:["ph",'pw'],
mounted(){
    this.changePos()
    setInterval(this.changePos,2000)
},methods:{
    changePos(){
        // console.log("gh")
      let  y=Math.floor(Math.random() * this.ph); 
      let  x=Math.floor(Math.random() * this.pw); 
    //   console.log(this.$el.style.top," y",y," w",this.pw," x",x," l",this.$el.style.left)
      this.$el.style.top=y+'px';
      this.$el.style.left=x+'px'
    }
}
}
</script>
<style scoped>
div{
    position: absolute;
    width: 20px;
    height: 20px;
    background: rosybrown;
    border-radius: 50%;
    transition: all 3s;
}
</style>