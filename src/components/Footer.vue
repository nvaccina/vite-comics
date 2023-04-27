<script>
import {footerMenu} from "../data/menu";

export default {
  name: 'Footer',

  data(){
    return{
      footerMenu,
    }
  }

}
</script>

<template>

  <footer>

    <div class="top">
      <div class="container">
        <div class="menu_footer">

          <div class="col">
            <nav>
              <h3>Dc Comics</h3>
              <ul>
                <li 
                  v-for="(link, index) in footerMenu.dcComics" 
                  :key="index"
                >
                  <a :href="link.href">{{ link.text }}</a>
                </li>
              </ul>
            </nav>
            <nav>
              <h3>Shop</h3>
              <ul>
                <li 
                  v-for="(link, index) in footerMenu.shop" 
                  :key="index"
                >
                  <a :href="link.href">{{ link.text }}</a>
                </li>
              </ul>
            </nav>

          </div>

          <div class="col">
            <nav>
              <h3>Dc</h3>
              <ul>
                <li 
                  v-for="(link, index) in footerMenu.dc" 
                  :key="index"
                >
                  <a :href="link.href">{{ link.text }}</a>
                </li>
              </ul>
            </nav>
          </div>

          <div class="col">
            <nav>
              <h3>Sites</h3>
              <ul>
                <li 
                  v-for="(link, index) in footerMenu.sites" 
                  :key="index"
                >
                  <a :href="link.href">{{ link.text }}</a>
                </li>
              </ul>
            </nav>
          </div>
          
        </div>

        <div class="big_logo">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>

      </div>

    </div>
    <div class="bottom">
        
    </div>

  </footer>
  
</template>


<style lang="scss" scoped>
@use '../scss/general/general' as *;
@use '../scss/general/mixin' as *;
@use '../scss/general/variables' as *;

.top{
  max-height: 300px;
  background-image: url(../assets/img/footer-bg.jpg);
  .container{
    @include centerFlex('between');
    .menu_footer{
      @include centerFlex('horizontal');
      .col{
        padding: 20px 20px;

        h3{
        text-transform: uppercase;
        padding: 10px 0;
        }
        
        a{
          color: #959595;
          font-size: 12px;
          &:hover{
            text-decoration: underline;
          }
        }
      
      }
    }
    .big_logo{
      @include centerFlex('vertical');
      height: 300px;
      overflow: hidden;
      
      img{
        width: 450px;
      }
    }
    
    

  }
  
  
}
</style>