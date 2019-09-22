<template>
<div class="container" >
    <div class="row w-100 h-100 no-gutters">
        <div class="col"><div class="card">
  <!-- <img src='../../assets/images/p (1).jpg' class="card-img-top" > -->
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
  </div>
</div></div>
        <div class="col">
            
    <img src='../../assets/images/p (1).jpg' class="card-img-top h-100"  >
        </div>
    </div>
    
</div>
</template>

<script>
export default {

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1140px
);
.container{
  
    width: 100vh
}
@media only screen and (min-width: 540px) {
  .container{
    width: 100vh
  }
}
@media only screen and (min-width: 720px) {
  .container{
    width: 50vh
  }
}
@media only screen and (min-width: 960px) {
 .container{
   width: 33.33vh;
 }
}
@media only screen and (min-width: 1140px) {
  .container{
   width: 25vh;
 }
}
</style>