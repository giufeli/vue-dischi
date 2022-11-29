<template>
  <div class="navBar">
    <div class="logo">
      <img
        src="@/assets/logo-spotify.png"
        alt=""
      >
    </div>
    <label for="LabelGenre">
      <select
        id="genre"
        name="genre"
        @change="$emit('selectgen', 'test')"
      >
        <option value="all">
          All
        </option>
        <option value="rock">
          Rock
        </option>
        <option value="pop">
          Pop
        </option>
        <option value="jazz">
          Jazz
        </option>
        <option value="metal">
          Metal
        </option>
      </select>
    </label>
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
    display: flex;
    align-items: center;
    justify-content:space-between ;
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
  label{
    float: right;
    margin-right: 100px;
  }

  select{
    width: 120px;
    padding: 5px;
    border-radius: 10px;
    text-align: center;
  }

</style>
