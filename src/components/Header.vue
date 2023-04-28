<script>

import {mainMenu} from "../data/menu";

export default {
  name: 'Header',

  data(){
    return{
      mainMenu,

    }
  }

}
</script>

<template>
  <header>
    <div class="container ht-80">

      <div class="logo">
        <a href="#">
          <img src="../assets/img/dc-logo.png" alt="Logo Dc">
        </a>
        
      </div>

      <nav class="ht-80">
        <ul class="ht-80">
          <li 
            class="ht-80"
            v-for="(link, index) in mainMenu" 
            :key="index"
          >
            <a 
              class="ht-80"
              :href="link.href" 
              :class="{'active' : link.isActive}"
              >{{ link.text }}</a>
          </li>
        </ul>

      </nav>

    </div>
    
  </header>
  
</template>


<style lang="scss" scoped>
@use '../scss/general/general' as *;
@use '../scss/general/mixin' as *;
@use '../scss/general/variables' as *;

header{
  .container{
    @include centerFlex('between');
    height: 100%;
    .logo{
      width: 65px;
      &:hover{
        filter: brightness(10%);
      }
    }
    nav{
      ul{
        @include centerFlex('both');
        a{
          @include centerFlex('vertical');
          margin: 0 10px;
          text-transform: uppercase;
          font-weight: 600;
          font-size: 12px;
          color: #464646;
          border-bottom: 4px solid white;
          &:hover,
          &.active{
            color: $primary-color;
            border-color: $primary-color;
        }

        }
      }
      
    }

  }
  
}

</style>