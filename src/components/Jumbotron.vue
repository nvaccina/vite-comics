<script>
export default {
  name: 'Jumbotron',

}
</script>

<template>
  <div class="jumbotron"></div>
  
</template>

<style lang="scss" scoped>
@use '../scss/general/general' as *;
@use '../scss/general/variables' as *;
.jumbotron{
  height: 350px;
  background-size: cover;
  background-image: url(../assets/img/jumbotron.jpg);
}

</style>