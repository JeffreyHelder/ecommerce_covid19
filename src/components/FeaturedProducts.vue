<template>
  <div class="featured">
    <div class="container">
      <div class="sectionTitle">
        <h3>Protect Your Health</h3>
        <h2>Our Featured Products</h2>
      </div>
      <div class="products">
        <div v-for="product in products" :key="product.productId" class="product-box">
          <div class="image">
            <div class="saleTag">
              <img src="../assets/img/sale.png" alt="sale tag">
              <p>{{ product.sale }} <br> OFF</p>
            </div>
            <img :src="product.image" :alt="product.description">
            <div class="overlay">
              <div class="overlay-inner">
                <button>Add to Cart</button>
                <a href="#"><img src="../assets/img/view.png" alt="View Item"></a>
                <a href="#"><img src="../assets/img/heart.png" alt="Favorite Item"></a>
              </div>
            </div>
          </div>
          <div class="info">
            <h4>{{ product.name }}</h4>
            <div class="details">
              <p><b>{{ product.price }}</b> <em>{{ product.savings }}</em></p>
              <img :src="product.rating" :alt="product.ratingAlt">
            </div>
          </div>
        </div>
      </div>
      <div class="button">
        <button>View All Products</button>
      </div>
    </div>
    <img class="right-virus" src="../assets/img/virus.png" alt="virus icon">
    <img class="left-virus" src="../assets/img/virus.png" alt="virus icon">
  </div>
</template>

<script>
export default {
  name: 'FeaturedProducts',
  data: function() {
    return {
      products: [
        { 
          name: 'Customized Reusable Face Mask',
          description: 'Black Reusable Face Mask',
          price: '$20.00',
          savings: '$4.00',
          sale: '20%',
          rating: './img/4-5.png',
          ratingAlt: 'four and a half stars',
          productId: '1',
          image: './img/blackmask.png'
        },
        { 
          name: 'Young Vision Hand Sanitizer',
          description: 'Hand Sanitizer',
          price: '$30.00',
          savings: '$2.00',
          sale: '10%',
          rating: './img/3.png',
          ratingAlt: 'three stars',
          productId: '2',
          image: './img/youngvision.png'
        },
        { 
          name: 'Customized Reusable Face Mask',
          description: 'Grey Reusable Face Mask',
          price: '$35.00',
          savings: '$8.00',
          sale: '25%',
          rating: './img/3.png',
          ratingAlt: 'three stars',
          productId: '3',
          image: './img/greymask.png'
        },
        { 
          name: 'Young Vision Hand Sanitizer',
          description: 'Hand Sanitizer',
          price: '$25.00',
          savings: '$5.00',
          sale: '30%',
          rating: './img/4-5.png',
          ratingAlt: 'four and a half stars',
          productId: '4',
          image: './img/bluesanitizer.png'
        },
        { 
          name: 'Customized Reusable Face Mask',
          description: 'Light Blue Reusable Face Mask',
          price: '$10.00',
          savings: '$2.00',
          sale: '30%',
          rating: './img/4.png',
          ratingAlt: 'four stars',
          productId: '5',
          image: './img/lightbluemask.png'
        },
        { 
          name: 'Care Plus Medical Gloves',
          description: 'Medical Gloves',
          price: '$16.00',
          savings: '$5.00',
          sale: '15%',
          rating: './img/4-5.png',
          ratingAlt: 'four and a half stars',
          productId: '6',
          image: './img/bluegloves.png'
        }
      ]
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
.featured{
  max-width: 100vW;
  width: 100%;
  height: 100%;
  position: relative;

  // mobile-small //
  @media only screen and (max-width: 914px) {
    .container{
      width: 95% !important;
      .products{
        justify-content: space-around !important;
        .product-box{
          width: 90% !important;
          .image{
            width: 350px !important;
          }
          .info{
            width: 325px !important;
          }
        }
      }
    }
   .left-virus{
    opacity: .1;
    position: absolute;
    width: 30% !important;
    bottom: 0% !important;
    left: -22% !important;
  }
  }

  //medium-large//
  @media only screen and (max-width: 1100px) and (min-width: 915px) {
    .container{
      width: 95% !important;
      .products{
        justify-content: space-around !important;
        .product-box{
          width: 45% !important;
          .image{
            width: 350px !important;
          }
          .info{
            width: 325px !important;
          }
        }
      }
    }
  }

  .container{
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    width: 85%;
    max-width: 1600px;
    margin: auto;
    height: 100%;
    .sectionTitle{
      h3{
        line-height: 1;
        padding: 0;
        margin: 0;
        margin-top: 50px;
        font-size: 1.2rem;
        font-weight: 200;
      }
      h2{
        font-size: 1.8rem;
        line-height: 1;
        margin: 25px 0;
      }
    }
    .products{
      margin-top: 20px;
      max-width: 1290px;
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: space-between;

      .product-box{
        width: 30%;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 50px;
        .image{
          display: flex;
          width: 300px;
          height: 250px;
          background-color: #F5F5F5;
          position: relative;
          .overlay{
            opacity: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba($color: #E5F1F5, $alpha: .6);
            z-index: 949;
            transition: .3s;
            .overlay-inner{
              display: flex;
              justify-content: space-between;
              flex-wrap: wrap;
              width: 45%;
              button{
                width: 100%;
                margin-bottom: 10px;
                height: 40px;
                background-color: #ff6d33;
                font-size: .85rem;
                font-weight: 500;
                color: white;
                border: 3px solid white;
                cursor: pointer;
              }
              a{
                width: 40%;
                img{
                  max-width: 100%;
                }
              }
            }
          }
          &:hover{
            .overlay{
              opacity: 1;
            }
          }
          img{
            margin: auto;
            align-self: center;
            max-width: 80%;
            max-height: 90%;
          }
          .saleTag{
            position: absolute;
            width: 40px;
            z-index: 950;
            p{
              line-height: 1.2;
              margin: 0;
              position: absolute;
              top: 5%;
              left: 20%;
              font-size: .65rem;
              color: white;
              font-weight: normal;
            }
          }
        }
        .info{
          text-align: left;
          display: flex;
          flex-direction: row;
          flex-wrap: wrap;
          width: 275px;
          cursor: pointer;
          h4{
            font-weight: 400;
          }
          .details{
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            width: 100%;
            p{
              line-height: 1;
              margin: 0;
              em{
                font-size: .8rem;
                font-weight: 200;
                color: grey;
                text-decoration: line-through;
              }
              b{
                font-size: 1.2rem;
                color: #ff6d33;
                font-style: normal;
                font-weight: 600;
              }
            }
            img{
              max-width: 100%;
              max-height: 60%;
            }
          }
        }
      }
    }
    .button{
      margin-bottom: 50px;
      margin-top: 20px;
      button{
        width: 300px;
        height: 60px;
        background-color: #ff6d33;
        font-size: .9rem;
        font-weight: 500;
        color: white;
        border: 3px solid white;
        cursor: pointer;
      }
    }
  }
  .right-virus{
    opacity: .1;
    position: absolute;
    width: 18%;
    top: 0;
    right: -10%;
  }
  .left-virus{
    opacity: .1;
    position: absolute;
    width: 14%;
    bottom: 60%;
    left: -8%;
  }
}

</style>
