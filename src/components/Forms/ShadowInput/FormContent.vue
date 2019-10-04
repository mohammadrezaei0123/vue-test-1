<template>
  <div class="w-100 bg-danger" style="height:500px;z-index:0">
      <shadow-content :zIndex="zIndexShadow" @closeShadow="isFocused"></shadow-content>
      <input-shadow :zIndex="zIndexInput" @isFocused="isFocused"></input-shadow>
      
      <input-shadow :zIndex="zIndexInput" @isFocused="isFocused"></input-shadow>
  </div>
</template>

<script>
import ShadowContent from "./ShadowContent";
import InputShadow from "./InputShadow";
export default {
    components:{
        ShadowContent,InputShadow
    },
    data(){
        return{
            zIndexShadow:-1,
            zIndexInput:2
        }
    },
    methods:{
        isFocused(){
            console.log("value")
            this.zIndexShadow*=-1;
            // this.zIndexInput*=-1;
        }
    }

}
</script>

<style scoped>

</style>