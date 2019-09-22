<template>
<div class="d-flex">
    <button v-on:click="show = !show">
    Toggle
    
  </button>
  <transition name="fade">
    <p v-if="show">hello ffffffffffffffffffffffffffffff 
    </p>
  </transition>
</div>
</template>

<script>
export default {
  data(){return{
    show: true
  }}
}
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

/* Safari 4.0 - 8.0 */
@-webkit-keyframes mymove {
  0% {left: -100%;}
  100% {left: 100%;}
}

@keyframes mymove {
  0% {left: -100%;}
  100% {left: 100%;}
}
.text-a{
    color: blueviolet;
-webkit-animation: mymove 5s infinite; /* Safari 4.0 - 8.0 */
  animation: mymove 5s infinite;
}
</style>