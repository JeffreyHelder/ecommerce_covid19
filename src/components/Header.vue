<template>
  <div class="header">
    <div class="container">
      <img class="logo" src="../assets/img/Logo.png" alt="covid-19 logo">
      <div class="top-nav">
        <ul>
          <li><a class="active" href="#">Home</a></li>
          <li><a href="#">About us</a></li>
          <li><a href="#">Product view</a></li>
          <li><a href="#">Shop now</a></li>
          <li><a href="#">Contact us</a></li>
          <li><a class="cart" href="#"><img src="../assets/img/cart.png" alt="cart"></a></li>
        </ul>
        <button>Sign up</button>
      </div>
      <a v-on:click="mobileNav = !mobileNav" class="menu-toggle">
        <p v-if="mobileNav == false">menu</p>
        <p v-if="mobileNav == true">close</p>
      </a>
    </div>
    <div v-if="mobileNav == true" class="mobile-nav">
      <ul>
        <li><a class="active" href="#">Home</a></li>
        <li><a href="#">About us</a></li>
        <li><a href="#">Product view</a></li>
        <li><a href="#">Shop now</a></li>
        <li><a href="#">Contact us</a></li>
        <li><a class="cart" href="#"><img src="../assets/img/cart.png" alt="cart"></a></li>
      </ul>
      <button>Sign up</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data: function() {
    return {
      mobileNav: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.header{
  //mobile-medium//
  @media only screen and (max-width: 914px) {
    .container{
      width: 95% !important;
      margin: 0 2.5%!important;
      height: 45px !important;
      padding-top: 10px !important;
      z-index: 999;
      .menu-toggle {
        cursor: pointer;
        display: block !important;
        color: black;
      }
      .top-nav ul, button{
        display: none !important;
      } 
    }
    .mobile-nav{
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-around;
      position: fixed;
      width: 100vW;
      height: 100vH;
      background-color: #FFF7F5;
      right: 0;
      z-index: 950;

      ul{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        height: 50vH;
        margin-top: 60px;
        list-style: none;
        padding: 0;
        margin-bottom: 30px;
        li{
          a{
            padding: 10px 25px;
            font-weight: 500;
            text-decoration: none;
            color: #3A393E;
          }
          .cart{
            padding: 0;
            height: 35px !important;
            width: 38px !important;
            background-color: white;
            display: flex;
            align-items: center;
            justify-content: center;
          }
        }
        li .active{
          color: #FF6D33 !important;
        }
      }
      button{
        height: 50px;
        width: 150px;
        background-color: #ff6d33;
        font-size: .8rem;
        font-weight: 500;
        color: white;
        border: 4px solid white;
        margin-bottom: 120px;
      }
    }
  }

  //medium-large//
  @media only screen and (max-width: 1100px) and (min-width: 915px) {
    .container{
      width: 95% !important;
      height: 55px !important;
      .top-nav ul{
        margin-right: 0px !important;
        li {
          a {
            padding: 10px 18px !important;
          }
          .cart{
            height: 30px !important;
            width: 34px !important;
            margin-right: 20px;
          }
        }
      } 
    }
  }

  *{
    font-family: source-han-sans-traditional, sans-serif;
  }

  font-size: .8rem;
  max-width: 100vW;
  width: 100%;
  position: fixed;
  background-color: #FFF7F5;
  z-index: 999;

  .container{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin: auto;
    margin-top: 15px;
    width: 85%;
    height: 65px;
    max-width: 1600px;

    .logo{
      align-self: flex-start;
      max-width: 90%;
      max-height: 90%;
    } 
    .top-nav, .top-nav ul, .top-nav ul li {
      display: flex;
      flex-direction: row;
    }
    .top-nav {
      ul {
        height: 45px;
        margin-top: 0;
        margin-right: 20px;

        li {
          align-items: center;
          a {
            font-weight: 500;
            text-decoration: none;
            color: #3A393E;
            padding: 10px 24px;
            &:hover{
              color: #FF6D33;
            }
          }
          .cart {
            padding: 0 !important;
            height: 35px;
            width: 38px;
            background-color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            img{
              width: 14px;
              height: 15px;
            }
          }
        }

        li .active{
          color: #FF6D33 !important;
        }
      }
      button{
        height: 45px;
        width: 110px;
        background-color: #ff6d33;
        font-size: .8rem;
        font-weight: 500;
        color: white;
        border: 4px solid white;
      }
    }
    .menu-toggle{
      display: none;
    }
  }
}
</style>
