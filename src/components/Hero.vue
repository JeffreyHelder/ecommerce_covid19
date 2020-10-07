<template>
  <div class="hero">
    <div class="container">
      <div class="message">
        <h3><em>covid-19</em> Be Aware Of Coronavirus</h3>
        <h1>Protect Yourself <br> From <em>Virus.</em></h1>
        <p>Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer tookng.</p>
        <button>View Product</button>
      </div>
      <div class="image">
        <img src="../assets/img/woman.png" alt="masked woman with arms crossed">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
*{
  font-family: source-han-sans-traditional, sans-serif;
  color: black;
}
.hero{
    //mobile-medium//
  @media only screen and (max-width: 914px) {
    height: 100vH !important;
    transform: translateY(0) !important;
    .container{
      width: 94% !important;
      flex-direction: column !important;
      height: 100vH !important;
      overflow: hidden;
      padding-top: 0 !important;
      .message{
        margin-top: 60px !important;
        width: 90% !important;
        h1{
          font-size: 2rem !important;
        }
      }
      .image{
        right: 0;
        width: 60% !important;
        position: absolute;
      }
    }
  }

  //medium-large//
  @media only screen and (max-width: 1100px) and (min-width: 915px) {
    .container{
      width: 94% !important;
      justify-content: space-around !important;
      .message{
        width: 40% !important;
      }
      .image{
        width: 50% !important;
      }
    }
  }
  max-width: 100vW;
  width: 100%;
  height: 100%;
  background-color: #FFF7F5;
  transform: translateY(-11vH);

  .container{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 85%;
    max-width: 1600px;
    margin: auto;
    padding-top: 10vH;
    height: 100%;

    .message{
      width: 40%;
      text-align: left;
      justify-self: flex-start;
      h3{
        font-size: .9rem;
        font-weight: 200;
        em{
          font-style: normal;
          text-transform: uppercase;
          color: #ff6d33;
        }
      }
      h1{
        margin: 0;
        font-size: 2.5rem;
        em{
          font-style: normal;
          color: #ff6d33;
        }
      }
      p{
        font-size: .9rem;
        font-weight: 200;
        margin-bottom: 40px;
        max-width: 430px;
      }
      button{
        height: 45px;
        width: 140px;
        background-color: #ff6d33;
        font-size: .8rem;
        font-weight: 500;
        color: white;
        border: 4px solid white;
      }
    }

    .image{
      display: flex;
      align-items: flex-end;
      height: 100%;
      width: 40%;
      img{
        max-width: 100%;
        max-height: 100%;
      }
    }
  }
}

</style>
