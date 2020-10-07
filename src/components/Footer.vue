<template>
  <div class="footer">
    <div class="container">
     <div class="info">
       <img class="logo" src="../assets/img/Logo.png" alt="Covid logo">
       <p>
          Lorem Ipsum has been the industry's 
          standard dummy text ever since the 
          1500s, when an unknown.
        </p>
        <ul>
          <li><a href="#"><img src="../assets/img/Icon-facebook.png" alt="facebook icon"></a></li>
          <li><a href="#"><img src="../assets/img/Icon-twitter.png" alt="twitter icon"></a></li>
          <li><a href="#"><img src="../assets/img/Icon-Youtube.png" alt="youtube icon"></a></li>
          <li><a href="#"><img src="../assets/img/Icon-linkedin.png" alt="linkedin icon"></a></li>
        </ul>
     </div>
     <div class="links">
       <h4>Links</h4>
       <ul>
         <li><a href="#">Shop</a></li>
         <li><a href="#">Product</a></li>
         <li><a href="#">Collection</a></li>
         <li><a href="#">About Corona</a></li>
         <li><a href="#">Company</a></li>
         <li><a href="#">Blog</a></li>
       </ul>
     </div>
     <div class="support">
       <h4>Company Support</h4>
       <ul>
         <li><a href="#">Maintenance</a></li>
         <li><a href="#">Support</a></li>
         <li><a href="#">Reviews</a></li>
         <li><a href="#">Contact us</a></li>
         <li><a href="#">Privacy policy</a></li>
         <li><a href="#">Frequently Asked Questions</a></li>
         </ul>
     </div>
     <div class="instagram">
       <h4>Follow us on Instagram</h4>
       <ul>
         <li data-post="1"><a href="#"><img src="../assets/img/instagram1.png" alt="instagram post"></a></li>
         <li data-post="2"><a href="#"><img src="../assets/img/instagram2.png" alt="instagram post"></a></li>
         <li data-post="3"><a href="#"><img src="../assets/img/instagram3.png" alt="instagram post"></a></li>
         <li data-post="4"><a href="#"><img src="../assets/img/instagram4.png" alt="instagram post"></a></li>
         <li data-post="5"><a href="#"><img src="../assets/img/instagram5.png" alt="instagram post"></a></li>
         <li data-post="6"><a href="#"><img src="../assets/img/instagram6.png" alt="instagram post"></a></li>
       </ul>
     </div>
    </div>
    <div class="copyright">
      <p>&#169; Copyright, Company, 2020</p>
    </div>
    <img class="mid-virus" src="../assets/img/virus.png" alt="virus icon">
    <img class="right-virus" src="../assets/img/virus.png" alt="virus icon">
    <img class="left-virus" src="../assets/img/virus.png" alt="virus icon">
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data: function() {
    return {
      mobileNav: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
*{
  font-family: source-han-sans-traditional, sans-serif;
  color: black;
}
* ul, * a {
  list-style: none;
  text-decoration: none;
  &:hover{
    color: #ff6d33;
  }
}
.footer{
  //mobile-medium//
  @media only screen and (max-width: 914px) {
    z-index: 950 !important;
    .container{
      flex-wrap: wrap;
      width: 90% !important;
      align-items: center !important;;
      .info{
        order: 1;
        width: 100% !important;
        padding-bottom: 10px;
        p{
          font-size: .8rem !important;
          max-width: 400px;
        }
        .logo{  
          max-height: 75% !important;
          max-width: 75% !important;
        }
        ul {
          width: 100% !important;
          max-width: 200px;
          li a img{
            width: 100% !important;
          }
        }
      }
      .links{
        order: 3;
        width: 40% !important;
        padding-left: 10px;
        padding-top: 10px;
        h4{
          font-size: 1rem !important;
          margin-top: 0;
        }
        ul{
          font-size: .8rem !important;
        }
      }
      .support{
        order: 4;
        width: 50% !important;
        padding-top: 10px;
        h4{
          font-size: 1rem !important;
          margin-top: 0;
        }
        ul{
          font-size: .8rem !important;
        }
      }
      .instagram{
        order: 2;
        width: 90% !important;
        padding-bottom: 10px;
        padding-top: 10px;
        h4{
          font-size: 1rem !important;
          margin-top: 0;
          padding: 0 !important;
        }
        ul{
          padding: 0;
          justify-content: space-between !important;
          li[data-post="6"], li[data-post="5"], li[data-post="4"], li[data-post="3"] {
            display: none;
          }
          li{
            display: flex;
            width: 40% !important;
            padding: 0 !important;
          }
        }
      }
    }
    .mid-virus{
      width: 20% !important;
    }
    .right-virus{
      width: 15%  !important;
      bottom: 0  !important;
      right: -5%;
    }
    .left-virus{
      width: 20%  !important;
      top: 10%  !important;
      left: 90%  !important;
    }
  }

  //medium-large//
  @media only screen and (max-width: 1100px) and (min-width: 915px) {
    .container{
      .info{
        width: 30% !important;
        .logo{  
          max-height: 75% !important;
          max-width: 75% !important;
        }
      }
      .support{
        width: 25% !important;
      }
      .instagram{
        width: 30% !important;
        ul{
          
        padding: 0;
          li[data-post="5"], li[data-post="2"] {
            display: none;
          }
          li{
            width: 40% !important;
            padding: 10px !important;
          }
        }
      }
    }
  }

  font-size: .8rem;
  display: flex;
  flex-direction: column;
  position: relative;
  max-width: 100vW;
  width: 100%;
  height: 100%;
  z-index: 999;
  bottom: 0;
  background-color: #FFF7F5;

  .container{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin: auto;
    margin-top: 40px;
    margin-bottom: 10px;
    width: 85%;
    max-width: 1600px;

    .info{
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      width: 25%;
      text-align: left;
      .logo{
        max-height: 50%;
        max-width: 50%;
        margin-bottom: 10px;
      }
      p{
        width: 75%;
        font-size: .65rem;
        font-weight: 200;
      }
      ul {
        padding: 0;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 55%;
        li a img{
          width: 65%;
        }
      }
    }
    .links{
      width: 15%;
      text-align: left;
      ul {
        font-size: .7rem;
        font-weight: 200;
        padding: 0;
        text-align: left;
        li{ 
          padding-bottom: 8px;
        }
      }
    }
    .support{
      width: 15%;
      text-align: left;
       ul {
        font-size: .7rem;
        font-weight: 200;
        padding: 0;
        text-align: left;
        li{ 
          padding-bottom: 8px;
        }
      }
    }
    .instagram{
      width: 45%;
      h4{
        padding-left: 60px;
        text-align: left;
      }
      ul{
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-around;
        li{
          width: 25%;
          padding: 10px;
          a img {
            max-height: 100%;
            max-width: 100%;
          }
        }
      }
    }
  }
  .copyright{
    width: 100vW;
    height: 35px;
    p{
      font-size: .6rem;
      font-weight: 200;
      margin: 0;
    }
  }
  .mid-virus{
    opacity: .1;
    position: absolute;
    width: 10%;
    top: 62%;
    left: 20%;
    z-index: -1;
  }
  .right-virus{
    opacity: .1;
    position: absolute;
    width: 10%;
    bottom: 10%;
    right: -5%;
  }
  .left-virus{
    opacity: .1;
    position: absolute;
    width: 8%;
    top: 0;
    left: -3%;
  }
}
</style>
