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
      <div class="button_load">
          <a href="#">LOAD MORE</a>
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
      margin-bottom: 45px;
      
    }
    .button_load{
      position: absolute;
      left: 50%;
      bottom: -50px;
      transform: translate(-50%);
      text-align: center;
      cursor: pointer;
      font-weight: 700;
      padding: 5px 40px;
      background-color: $primary-color;
      &:hover{
        background-color: $secondary-color;
        a{
          color: $primary-color;
        }
      }
      a{
        color: $secondary-color;
        font-size: 12px;
      }
    }
  }
}

</style>