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
              <h4>Dc Comics</h4>
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
              <h4>Shop</h4>
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
              <h4>Dc</h4>
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
              <h4>Sites</h4>
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
          <h4>follow us</h4>
          <nav>
            <ul>
              <li 
                v-for="(icon, index) in footerIcon" 
                :key="index"
              >
                <a :href="icon.href">
                  <img :src="icon.image" alt="">
                </a>
              </li>
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
  min-height: 300px;
  background-image: url(../assets/img/footer-bg.jpg);
  .container{
    @include centerFlex('between');
    .menu_footer{
      @include centerFlex('horizontal');
      .col{
        padding: 20px 20px 20px 0;
        h4{
        text-transform: uppercase;
        padding: 10px 0;
        }
        a{
          color: #959595;
          font-size: 12px;
          &:hover{
            color: $primary-color;
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
        font-size: 14px;
      }
    }
    .social{
      @include centerFlex('both');
      h4{
        color: $primary-color;
        font-weight: 700;
        text-transform: uppercase;
        padding-right: 10px
      }
      nav{
        ul{
          @include centerFlex('both');
          a{
            @include centerFlex('vertical');
            padding: 0 10px;
            width: 50px;
            &:hover{
              filter: invert(200%) brightness(200%);
            }
          }
        }
      
    }
    }
  }
}
</style>