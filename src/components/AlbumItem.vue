<template>
  <div class="col">
    <div class="albumBox">
      <div class="imgBox">
        <img
          :src="imgUrl"
          :alt="title"
        >
      </div>
      <div class="title">
        {{ title }}
      </div>
      <div class="author">
        {{ author }}
      </div>
      <div class="year">
        {{ year }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    imgUrl: String,
    title: String,
    author: String,
    year: String,
  },
};
</script>

<style style lang="scss" scoped>
  .albumBox{
    background-color: rgba(46,58,70,255);
    margin-top: 50px;
    width: 210px;
    height: 330px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    text-align: center;
    border-radius: 8px;
  }
  .imgbox{
    display: flex;
    flex-direction: column;
    justify-content: end;
    width: 100%;
    height: 50%;
  }

  img{
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  .title{
    font-size: 20px;
    font-weight: 700;
    margin-top: 10px;
    margin-bottom: 15px;
  }

  .author, .year{
    font-size: 15px;
    color: rgb(160, 160, 160);
  }
</style>
