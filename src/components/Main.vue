<script>

import Cards from './partials/Cards.vue';
import DcComics from '../data/dc-comics.json'

export default {
  name: 'Main',
  components:{
    Cards,
  },
  data(){
    return{
      DcComics,
    }
  }

}
</script>

<template>

  <main>
    <div class="container">
      <h4>current series</h4>

      <div class="cards-wrapper">

        <Cards
          v-for="(card, index) in DcComics"
          :key="index"
          :image="card.thumb"
          :nameSeries="card.series"
        />

      </div>
    </div>
  </main>
  
</template>


<style lang="scss" scoped>
@use '../scss/general/general' as *;
@use '../scss/general/mixin' as *;
@use '../scss/general/variables' as *;

main{
  background-color: #1C1C1C;
  min-height: 150px;
  padding: 30px 0;
  .container{
    position: relative;
    
    h4{
      position: absolute;
      top: -50px;

      text-transform: uppercase;
      padding: 10px;
      background-color: $primary-color;
    }
    .cards-wrapper{
      display: flex;
      flex-wrap: wrap;
      
    }
  }
}

</style>