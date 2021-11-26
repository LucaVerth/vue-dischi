<template>

  <div class="col-sm-3 col-lg-2 album-card">
    <div class="album-cover">
      <img :src="album.poster" :alt="album.title">
    </div>
    <h5>{{album.title}}</h5>
    <span>{{album.author}}</span>
    <span>{{album.year}}</span>
  </div>
 
</template>

<script>
export default {
  name: 'Cards',
  props:{
    album: Object
  }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';
.album-card{
  display: flex;
  flex-direction:column;
  justify-content: flex-start;
  align-items: center;
  background-color: $primary-color;
  margin: 15px;
  .album-cover{
    //min-width: 40px;
    margin: 10px;
  }
  h5{
    color: #fff;
    text-transform: uppercase;
    font-size: 1rem;
  }
  span{
    color: grey;
  }
}
</style>