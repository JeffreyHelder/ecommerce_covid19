<template>
  <div class="testimonial-section">
    <div class="container">
      <div class="sectionTitle">
        <h3>Protect Your Health</h3>
        <h2>Our Beloved Customer</h2>
      </div>
      <div class="testimonials">
        <div class="testimonial-box" v-for="testimonial in testimonials" :key="testimonial.id">
          <img :src="testimonial.image" :alt="testimonial.name">
          <p>{{ testimonial.description }}</p>
          <p>{{ testimonial.name }}</p>
        </div>
        <img class="background" src="../assets/img/Bg.png" alt="background color">
        <img class="active-quote" src="../assets/img/quote.png" alt="quote mark">
        <img class="left-quote" src="../assets/img/quote.png" alt="quote mark">
        <img class="right-quote" src="../assets/img/quote.png" alt="quote mark">
      </div>
      <div class="carouselButtons">
        <ul>
          <li>◉</li>
          <li class="active">◉</li>
          <li>◉</li>
        </ul>
      </div>
    </div>
    <img class="left-virus" src="../assets/img/virus.png" alt="virus icon">
  </div>
</template>

<script>
export default {
  name: 'Testimonials',
  data: function() {
    return {
      testimonials: [
        { 
          name: 'Eduard Franz',
          description: "This is very best product lorem has been the industry's standard dummy text ever since to very the 1500s😍",
          image: './img/testimonial1.png',
          id: '1'
        },
        { 
          name: 'Abriella Bond',
          description: "This is very best product lorem has been the industry's standard dummy text ever since to very the 1500s👍",
          image: './img/testimonial2.png',
          id: '2'
        },
        { 
          name: 'Kinslee Fink',
          description: "This is very best product lorem has been the industry's standard dummy text ever since to very the 1500s🧡",
          image: './img/testimonial3.png',
          id: '3'
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
.testimonial-section{
  max-width: 100vW;
  width: 100%;
  height: 100%;
  position: relative;
  margin-bottom: 100px;

  
      
 @media only screen and (max-width: 915px) {
    .left-quote, .right-quote, .active-quote{
      display: none;
    }
    .background{
      left: 120% !important;
      margin-top: -175px;
      margin-left: -175px;
    }
 }
  //medium-large//
  @media only screen and (max-width: 1100px) {
    .container{
      width: 100% !important;
      .testimonials{
        justify-content: flex-start !important;
        width: 100% !important;
        .testimonial-box{
          width: 45% !important;
          .info{
            width: 325px !important;
          }
        }
      }
    }
    .left-virus{
      width: 25% !important;
      top: 0;
      left: -10%;
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
    margin-bottom: 50px;
    height: 100%;
    .sectionTitle{
      margin-bottom: 20px;
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
    .testimonials{
      padding-top: 30px;
      padding-bottom: 30px;
      height: 300px;
      width: 100%;
      max-width: 1290px;
      display: flex;
      flex-direction: row;
      position: relative;
      justify-content: space-between;
      align-items: center;
      overflow-x: scroll;
      overflow-y: hidden;
      &::-webkit-scrollbar {
          background: transparent;  /* Optional: just make scrollbar invisible */
      }
      .testimonial-box{
        min-width: 250px;
        padding: 0 20px;
        display: flex;
        flex-direction: column;
        align-items: center;
        img{
          width: 30%;
          align-self: center;
          justify-self: center;
        }
        p{
          font-size: .8rem;
          margin-bottom: 5px;
        }
      }
      .background{
        position: absolute;
        width: 350px;
        top: 50%;
        left: 50%;
        margin-top: -175px;
        margin-left: -175px;
        z-index: -1;
      }
      .active-quote, .left-quote, .right-quote {
        position: absolute;
        top: 10px;
      }
      .left-quote, .right-quote{
        opacity: .25;
      }
      .active-quote{
        left: 55%;
      }
      .left-quote{
        left: 25%;
      }
      .right-quote{
        right: 5%;
      }
    }
    .carouselButtons{
      width: 100%;
      ul{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        list-style: none;
        margin: auto;
        padding: 0;
        width: 50%;
        max-width: 150px;
        font-size: 1.3rem;
        li{
          cursor: pointer;
          color: lightgrey;
        }
        .active{
          color: #ff6d33 !important;
        }
      }
    }
  }
  .left-virus{
    opacity: .1;
    position: absolute;
    width: 20%;
    top: 0;
    left: -10%;
  }
}

</style>
