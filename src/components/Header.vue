<template>
  <header>
    <div class="header-logo">
      <img src="../assets/img/logo-small.svg" alt="">
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

header{
  @include align();
  height: 70px;
  background-color: $primary-color;
}
.header-logo {
  width: 60px;
  height: 60px;
  padding: 10px;
}
</style>