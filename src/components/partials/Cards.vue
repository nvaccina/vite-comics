<script>
export default {
  name: 'Cards',
  props:{
    image: String,
    nameSeries: String,
  }

}
</script>

<template>

  <div class="card">
    <div class="image_container">
      <img :src="image" alt="nameSeries">
    </div>
    
    <p>{{nameSeries}}</p>
  </div>
  
</template>

<style lang="scss" scoped>
@use '../../scss/general/general' as *;
@use '../../scss/general/mixin' as *;
@use '../../scss/general/variables' as *;

.card{
  width: calc(100% / 6 - 30px);
  min-height: 100px;
  margin: 15px;
  .image_container{
    height: 200px;
    overflow: hidden;
  }
  p{
    text-transform: uppercase;
    font-size: 12px;
    color: $secondary-color;
    padding-top: 10px;

  }
}

</style>