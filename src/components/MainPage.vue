<template>
  <div class="bigbox">
    <div class="container text-white">
      <div class="row row-cols-5">
        {{ selectedfilter }}
        <AlbumItem
          v-for="i in arrAlbum"
          :key="i.id"
          :img-url="i.poster"
          :title="i.title"
          :author="i.author"
          :year="i.year"
        />
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import AlbumItem from '@/components/AlbumItem.vue';

export default {

  name: 'MainPage',
  components: {
    AlbumItem,
  },

  props: {
    selectedfilter: String,
  },

  data() {
    return {
      arrAlbum: null,
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
    };
  },
  created() {
    axios.get(this.urlApi)
      .then((axiosResponse) => {
        console.log(axiosResponse);
        this.arrAlbum = axiosResponse.data.response;
      });
  },
  methods: {
    filterGenere() {
      // const { genere } = document.getElementById('genre');
      this.$emit('change', 'test');
      // if (level === 'rock') {
      //  this.$emit('change');
      //  console.log('ciao');obj
      //  this.arrAlbum = '';
      // }
    },
  },
};

console.log(AlbumItem);
</script>

<style lang="scss" scoped>
  .bigbox{
    width: 100%;
    height: calc(100vh - 60px);
    background-color: rgba(30,45,59,255);
  }
</style>
