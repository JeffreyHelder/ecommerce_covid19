<template>
  <div class="group">
    <div class="container">
      <div data-box="1" class="product-container">
        <h2>Health Security Mask Collection</h2>
        <p>20% Off</p>
        <button>View Now</button>
        <img src="../assets/img/securityMaskCollection.png" alt="Health Security Mask Collection">
      </div>
      <div data-box="2" class="product-container">
        <h2>Best Hand Sanitizer Collection</h2>
        <p>40% Off</p>
        <button>View Now</button>
        <img src="../assets/img/bestHandSanitizerCollection.png" alt="Best Hand Sanitizer Collection">
      </div>
      <div data-box="3" class="product-container">
        <h2>Medical Gloves &amp; Sunglasses Collection</h2>
        <p>20% Off</p>
        <button>View Now</button>
        <img src="../assets/img/medicalGlovesAndGlasses.png" alt="Medical Gloves and Sunglasses Collection">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductGroup'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
*{
  font-family: source-han-sans-traditional, sans-serif;
  color: black;
}
.group{
  max-width: 100vW;
  width: 100%;
  height: 100%;

  .container{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    width: 85%;
    max-width: 1600px;
    margin: auto;
    height: 100%;
    div[data-box="1"]{
      background-color: #FCF0E7;
    }
    div[data-box="2"]{
      background-color: #E5F1F5;
    }
    div[data-box="3"]{
      background-color: rgba($color: #2684EF, $alpha: .10);
    }
    .product-container{
      margin: 20px;
      width: 25%;
      max-width: 310px;
      min-width: 230px;
      height: 150px;
      display: flex;
      flex-direction: column;
      position: relative;
      text-align: left;
      padding: 30px 20px;
      h2{
        font-size: 1rem;
        width: 75%;
        margin: 0;
        padding: 0;
      }
      p{
        padding: 0;
        margin: 0;
        font-size: .8rem;
        font-weight: 200;
      }
      button{
        margin-top: 30px;
        height: 40px;
        width: 100px;
        background-color: #ff6d33;
        font-size: .8rem;
        font-weight: 500;
        color: white;
        border: 3px solid white;
      }
      img{
        position: absolute;
        right: 0;
        bottom: 0;
        max-width: 55%;
        max-height: 175px;
      }
    }
  }
}

</style>
