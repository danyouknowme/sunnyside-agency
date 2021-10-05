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
        </div>
        <div class="image1"></div>
      </div>
      <div class="content1">
        <div class="image2"></div>
        <div class="text1">
          <h1>Transform your brand</h1>
          <span>
            We are a full-service creative agency specializing in helping brands grow fast. 
            Engage your clients through compelling visuals that do most of the marketing for you.
          </span>
          <a href="#">Learn more</a>
        </div>
      </div>
      <div class="content1">
        <div class="image3"></div>
        <div class="image4"></div>
      </div>
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