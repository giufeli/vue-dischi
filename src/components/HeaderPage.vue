<template>
  <div class="navBar">
    <div class="logo">
      <img
        src="@/assets/logo-spotify.png"
        alt=""
      >
    </div>
  </div>
</template>

<script>
export default {

};
</script>

<style style lang="scss" scoped>
  .navBar{
    width: 100%;
    height: 60px;
    background-color: rgba(46,58,70,255);
  }

  .logo{
    display: flex;
    float: left;
    align-items: center;
    margin-left: 20px;
    height: 100%;
  }

  img{
    width: 90%;
    height: 90%;
    object-fit: contain;
  }
</style>
