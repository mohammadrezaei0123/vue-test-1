<template>
  <input class="w-100 position-relative" :style="'z-index:'+z" @focus="focus">
</template>

<script>
export default {
    props:{
        zIndex:{
            type:Number,
            default:1
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
    methods:{
        focus(){
            console.log('fucosed')
            this.$emit("isFocused")
        }
    }
}
</script>

<style scoped>

</style>