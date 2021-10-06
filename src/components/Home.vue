<template>
  <div class="home">
    <div class="header">
      <div class="header-text">
        <span>We are creatives</span>
      </div>
      <div class="arrow-down">
        <router-link v-scroll-to="'#content'"><img src="../assets/icon-arrow-down.svg" alt=""></router-link>
      </div>
    </div>
    <div class="content" id="content">
      <div class="content1">
        <div class="text1">
          <h1>Transform your brand</h1>
          <span>
            We are a full-service creative agency specializing in helping brands grow fast. 
            Engage your clients through compelling visuals that do most of the marketing for you.
          </span>
          <a href="#">Learn more</a>
          <div class="rec1"></div>
        </div>
        <div class="image1"></div>
      </div>
      <div class="content1">
        <div class="image2"></div>
        <div class="text1">
          <h1>Stand out to the right audience</h1>
          <span>
            Using a collaborative formula of designers, researchers, photographers, videographers, and copywriters, we’ll build and extend your brand in digital places. 
          </span>
          <a href="#">Learn more</a>
          <div class="rec2"></div>
        </div>
      </div>
      <div class="content1">
        <div class="image3">
          <div class="text2">
            <h2>Graphic design</h2>
            <span>Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential clients’ attention.</span>
          </div>
        </div>
        <div class="image4">
          <div class="text2">
            <h2>Photography</h2>
            <span>Increase your credibility by getting the most stunning, high-quality photos that improve your business image.</span>
          </div>
        </div>
      </div>
    </div>
    <div class="testimonial" id="testimonial">
      <div class="head-text">
        <h2>Client Testimonials</h2>
      </div>
      <div class="people">
        <div class="person1">
          <img src="../assets/image-emily.jpg" alt="">
          <span>We put our trust in Sunnyside and they delivered, making sure our needs were met and deadlines were always hit.</span>
          <h3>Emily R.</h3>
          <h5>Marketing Director</h5>
        </div>
        <div class="person2">
          <img src="../assets/image-thomas.jpg" alt="">
          <span>Sunnyside’s enthusiasm coupled with their keen interest in our brand’s success made it a satisfying and enjoyable experience.</span>
          <h3>Thomas S.</h3>
          <h5>Chief Operating Officer</h5>
        </div>
        <div class="person3">
          <img src="../assets/image-jennie.jpg" alt="">
          <span>Incredible end result! Our sales increased over 400% when we worked with Sunnyside. Highly recommended!</span>
          <h3>Jennie F.</h3>
          <h5>Business Owner</h5>
        </div>
      </div>
    </div>
    <div class="mul-pic">
      <div class="pic1"></div>
      <div class="pic2"></div>
      <div class="pic3"></div>
      <div class="pic4"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
}
</script>

<style scoped>
  .home {
    width: 100vw;
    height: 100%;
  }

  .header {
    width: 100%;
    height: 100vh;
    background-image: url("../assets/desktop/image-header.jpg");
    background-repeat: no-repeat;
    background-position: bottom center;
    background-size: cover;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: -1;
  }

  .header-text {
    position: absolute;
    top: 20%;
    text-transform: uppercase;
    font-family: 'Fraunces', serif;
    color: #fff;
    font-size: 70px;
    letter-spacing: 15px;
  }

  .arrow-down img {
    position: relative;
    top: 30%;
    left: 50%;
    transform: translateY(-50%);
    cursor: pointer;
  }

  .content {
    width: 100%;
    height: 100%;
  }

  .content1 {
    display: flex;
    align-items: center;
  }

  .text1 {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: left;
    justify-content: space-between;
  }

  .image1 {
    flex: 1;
    background-image: url("../assets/desktop/image-transform.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    height: 720px;
    width: 600px;
  }

  .image2 {
    flex: 1;
    background-image: url("../assets/desktop/image-stand-out.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    height: 720px;
    width: 600px;
  }

  .image3 {
    flex: 1;
    background-image: url("../assets/desktop/image-graphic-design.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    height: 720px;
    width: 600px;
  }

  .image4 {
    flex: 1;
    background-image: url("../assets/desktop/image-photography.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    height: 720px;
    width: 600px;
  }

  .text1 h1 {
    font-family: 'Fraunces', serif;
    width: 40%;
    margin-right: 80px;
    color: hsl(212, 27%, 19%);
  }

  .text2 {
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
    margin-bottom: 100px;
  }

  .text2 h2 {
    position: relative;
    font-family: 'Fraunces', serif;
    color: hsl(212, 27%, 19%);
    bottom: 130px;
  }

  .text2 span {
    position: relative;
    bottom: 100px;
    width: 40%;
    color: hsl(213, 9%, 39%);
    line-height: 30px;
  }
  
  .text1 span {
    margin-top: 10px;
    width: 48%;
    color: hsl(232, 10%, 55%);
    line-height: 30px;
  }

  .text1 a {
    position: relative;
    right: 170px;
    font-family: 'Fraunces', serif;
    margin-top: 50px;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 16px;
    color: hsl(212, 27%, 19%);
  }

  .rec1 {
    position: relative;
    bottom: 6px;
    right: 170px;
    width: 122px;
    height: 6px;
    background: #F1E99F;
    mix-blend-mode: darken;
    border-radius: 10px;
  }

  .rec2 {
    position: relative;
    bottom: 6px;
    right: 170px;
    width: 122px;
    height: 6px;
    background: #F1BC9F;
    mix-blend-mode: darken;
    border-radius: 10px;
  }

  .testimonial {
    height: 900px;
    width: 100vw;
    background-color: #fff;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .head-text {
    font-size: 16px;
    position: relative;
    text-transform: uppercase;
    font-family: 'Fraunces', serif;
    color: hsl(210, 4%, 67%);
    letter-spacing: 7px;
    top: 20%;
    margin-bottom: 80px;
  }

  .people {
    height: 100%;
    width: 70%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .people img {
    width: 15%;
    border-radius: 50%;
    margin-bottom: 50px;
  }

  .people span {
    margin-top: 30px;
    width: 75%;
    line-height: 30px;
    color: hsl(213, 9%, 39%);
  }

  .people h3 {
    font-family: 'Fraunces', serif;
    position: relative;
    top: 50px;
    color: hsl(212, 27%, 19%);
  }

  .people h5 {
    position: relative;
    top: 10px;
    color: hsl(210, 4%, 67%);
  }

  .person1, .person2, .person3 {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .mul-pic {
    display: flex;
    width: 100vw;
    height: 596px;
  }

  .pic1 {
    width: 25%;
    background-image: url("../assets/desktop/image-gallery-milkbottles.jpg");
    background-size: contain;
  }

  .pic2 {
    width: 25%;
    background-image: url("../assets/desktop/image-gallery-orange.jpg");
    background-size: contain;
  }

  .pic3 {
    width: 25%;
    background-image: url("../assets/desktop/image-gallery-cone.jpg");
    background-size: contain;
  }

  .pic4 {
    width: 25%;
    background-image: url("../assets/desktop/image-gallery-sugarcubes.jpg");
    background-size: contain;
  }

  @media screen and (max-width: 375px) {
    .header {
      background-image: url("../assets/mobile/image-header.jpg");
      height: calc(100vh - 250px);
      width: 100vw;
    }

    .arrow-down img {
      position: absolute;
      top: 45%;
      left: 45%;
    }

    .header-text{
      position: static;
      display: flex;
      align-items: center;
      justify-content: flex-start;
      margin-bottom: 150px;
    }

    .header-text span{
      font-size: 32px;
      width: 100%;
    }

    .content1 {
      flex-direction: column-reverse;
    }

    .image1 {
      width: 100vw;
      height: 720px;
    }

  }
</style>