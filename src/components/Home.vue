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
  }

  .header-text {
    position: absolute;
    top: 20%;
    text-transform: uppercase;
    font-family: 'Fraunces', serif;
    color: #fff;
    font-size: 70px;
    letter-spacing: 15px;
    z-index: 1;
  }

  .arrow-down img {
    position: relative;
    top: 30%;
    left: 50%;
    transform: translateY(-50%);
    cursor: pointer;
  }

  .content {
    height: 100vh;
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
  }
</style>