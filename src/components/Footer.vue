<script>
import {footerMenu, footerIcon} from "../data/menu";

export default {
  name: 'Footer',

  data(){
    return{
      footerMenu,
      footerIcon,
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
    <div class="bottom ht-100">

      <div class="container ht-100">

        <div class="button_sign">
          <a href="#">SIGN-UP NOW!</a>
        </div>

        <div class="social">
          <h4>FOLLOW US</h4>
          <nav>
            <ul>
              <li 
                v-for="(link, index) in footerIcon" 
                :key="index"
              >
                <a :href="link.href"><img :src="link.src" alt=""></a></li>
            </ul>
          </nav>
        </div>

      </div>
        
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
        padding: 20px 20px 20px 0;

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
.bottom{
  background-color: #303030;
  .container{
    @include centerFlex('between');
    .button_sign{
      cursor: pointer;
      padding: 10px;
      border: 2px solid $primary-color;
      &:hover{
        background-color: $secondary-color;
        a{
          color: $primary-color;
        }
      }
      a{
        color: $secondary-color;
        font-weight: 600;
      }
    }
    .social{
      h4{
        color: $primary-color;
        font-weight: 700;
      }
      nav{
        ul{
          @include centerFlex('both');
          a{
            @include centerFlex('vertical');
            padding: 0 10px;
            text-transform: uppercase;
            font-weight: 600;
            font-size: 12px;
            
          }
        }
      
    }
    }
  }
}
</style>