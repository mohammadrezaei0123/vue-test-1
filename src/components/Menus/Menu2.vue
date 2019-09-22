<template>
  <div class="d-flex justify-content-between align-items-center w-100 px-3 py-1 bg-dark menus">
      <div class="brand"><img src="../../assets/images/p (1).jpg" alt="" srcset=""></div>
      <div class="items d-flex justify-content-center align-items-center">
          <h6 class="menu-items px-1 m-0">item1</h6>
          <h6 class="menu-items px-1 m-0">item1</h6>
          <h6 class="menu-items px-1 m-0">item1</h6>
          <h6 class="menu-items px-1 m-0">item1</h6>
          <h6 class="menu-items px-1 m-0">item1</h6>
          <h6 class="menu-items px-1 m-0">item1</h6>
      
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
.menus{
    min-height: 40px
}
 img{
     max-width: 40px;
     max-height: 40px;

 }
.menu-items{
    cursor: pointer;    
    &:hover{
        background:red;
    }
}
</style>