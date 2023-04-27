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
    <div class="container">

      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="Logo Dc">
      </div>

      <nav class="ht-100">
        <ul class="ht-100">
          <li 
            class="ht-100"
            v-for="(link, index) in mainMenu" 
            :key="index"
          >
            <a 
              class="ht-100"
              href="link.href" 
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
  text-align: center;
  height: 100px;
  .container{
    @include centerFlex('between');
    height: 100%;
    .logo{
      width: 65px;
    }
    nav{
      ul{
        @include centerFlex('both');
        a{
          display: inline-block;
          padding: 10px;
          text-transform: uppercase;
          font-weight: 600;
          color: #464646;
          margin-bottom: 3px solid white;
          &:hover,
          &.active{
            color: $primary-color;
            margin-bottom: 3px solid $primary-color;
        }

        }
      }
      
    }

  }
  
}

</style>