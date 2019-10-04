<template>
  <div class="h-100 w-100 position-fixed" @click="$emit('closeShadow')" :style="'top:0;left:0;right:0;bottom:0;background:rgba(0,0,0,0.4);z-index:'+z">

  </div>
</template>

<script>
export default {
    props:{
        zIndex:{
            type:Number,
            default:-1
            }
    },
    data(){
        return{
            z:this.zIndex
        }
    },
    watch:{
        zIndex(val){
            this.z=val
        }
    },
}
</script>

<style scoped>

</style>