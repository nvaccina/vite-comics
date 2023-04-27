<script>
import {buyAction} from "../data/menu";

export default {
  name: 'CallToAction',

  data(){
    return{
      buyAction
    }
  }

}
</script>

<template>

  <div class="action">
    <div class="container">
      <nav>
        <ul>
          <li 
            v-for="(link, index) in buyAction" 
            :key="index"
          >
            <a :href="link.href">
              <img :src="link.image" alt="">
              <span>{{ link.text }}</span>
            </a>
          </li>
        </ul>

      </nav>
    </div>
  </div>
  
</template>


<style lang="scss" scoped>
@use '../scss/general/general' as *;
@use '../scss/general/mixin' as *;
@use '../scss/general/variables' as *;

.action{
  background-color: $primary-color;
  min-height: 150px;
  padding: 30px 0;
  ul{
    @include centerFlex('both');
    li{
      margin: 0 20px;
      a{
        @include centerFlex('vertical');
        width: 40px ;
        height: 40px;
        
        img{
          height: 100%;
        }
    }
    }
    
  }
  
}

</style>