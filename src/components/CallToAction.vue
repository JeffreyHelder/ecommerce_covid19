<template>
  <div class="cta">
    <div class="container">
      <div class="content">
        <div class="info">  
          <h4><em>covid-19</em> Be Aware Of Coronavirus</h4>
          <h2>Corona Health Protection Safety Kit</h2>
          <p>Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer tookng.</p>
          <div class="buynow">
            <button>Buy Now</button>
            <p>Only for <em>$200.00</em></p>
          </div>
        </div>
        <img src="../assets/img/Kit.png" alt="Corona Health Protection Safety Kit">
      </div>
    </div>
    <img class="right-virus" src="../assets/img/virus.png" alt="virus icon">
  </div>
</template>

<script>
export default {
  name: 'CTA',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
*{
  font-family: source-han-sans-traditional, sans-serif;
  color: black;
}
.cta{
  margin-top: 40px;
  margin-bottom: 40px;
  width: 100%;
  height: 400px;
  background-image: url(/img/ctaBack.svg);
  background-position: right;
  background-size: cover;
  background-repeat: no-repeat;
  max-width: 1500px;
  position: relative;

  // mobile-small //
  @media only screen and (max-width: 914px) {
    .container{
      width: 95% !important;
      .content{
        flex-direction: column !important;
        justify-content: flex-start !important;
        align-items: flex-start !important;
        .info{
          width: 60% !important;
          h4{
            margin-top: 5px !important;
            font-size: .75rem !important;
            margin-bottom: 5px !important;
          }
          h2{
            font-size: 1rem !important;
            margin-top: 5px !important;
          }
          p{
            line-height: 1.2;
          }
          .buynow{
            margin-top: 10px !important;
            width: 100% !important;
          }
        }
        img{
          width: 60% !important;
          max-width: 286px !important;
        }
      }
    }
    .right-virus{
      width: 25% !important;
      top: -15% !important;
      right: -14% !important;
    }
  }

  //medium-large//
  @media only screen and (max-width: 1100px) and (min-width: 915px) {
    .container{
      width: 95% !important;
      .content{
        justify-content: flex-start !important;
        .info{
          width: 35% !important;
          p{
            font-size: .7rem !important;
          }
          .buynow{
            width: 90% !important;
          }
        }
        img{
          max-height: 80% !important;
        }
      }
    }
  }

  .container{
    display: flex;
    flex-direction: column;
    width: 85%;
    height: 100%;
    max-width: 1600px;
    margin: auto;
    .content{
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      height: 100%;
      .info{
        width: 40%;
        max-width: 375px;
        text-align: left;
        h4{
          margin-top: 0;
          font-size: .9rem;
          font-weight: 300;
          em{
            font-style: normal;
            text-transform: uppercase;
            color: #ff6d33;
          }
        }
        h2{
          font-weight: 600;
        }
        p{
          font-size: .8rem;
          font-weight: 200;
        }
        .buynow{
          display: flex;
          flex-direction: row;
          align-items: center;
          justify-content: space-between;
          width: 60%;
          margin-top: 30px;
          button{
            width: 100px;
            height: 35px;
            background-color: #ff6d33;
            font-size: .75rem;
            font-weight: 500;
            color: white;
            border: 3px solid white;
            cursor: pointer;
          }
          p{
            font-weight: 300;
            em{
            font-style: normal;
            color: #ff6d33;
            font-weight: 400;
            }
          }
        }
      }
      img{
        max-height: 95%;
      }
    }
  }
  .right-virus{
    opacity: .1;
    position: absolute;
    width: 12%;
    top: -25%;
    right: -5%;
    z-index: -1;
  }
}

</style>
