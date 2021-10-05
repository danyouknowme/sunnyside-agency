<template>
  <div class="navbar" v-bind:class="{ scrolled: isScrolled }">
    <div class="container">
      <div class="left">
        <img src="../assets/logo.svg" alt="" />
      </div>
      <div class="right">
        <span @click="toggleMenu(isPressed), isPressed = !isPressed" class="hamburger">
          <font-awesome-icon :icon="selectIcon(isPressed)"/>
        </span>
          <div class="menu">
            <a href="#">About</a>
            <a href="#">Services</a>
            <a href="#">Projects</a>
            <a href="#">Contact</a>
          </div>
      </div>
    </div>
    <div class="menu2">
      <a href="#">About</a>
      <a href="#">Services</a>
      <a href="#">Projects</a>
      <a href="#">Contact</a>
    </div>
  </div>
</template>
  

<script>
export default {
  name: "Navbar",
  props: {
    isScrolled: Boolean,
  },
  data() {
    return {
      isPressed: false,
    };
  },
  methods: {
    toggleMenu: function(isPressed) {
      if (!isPressed) {
        document.querySelector(".menu2").style.display = "flex";
      } else {
        document.querySelector(".menu2").style.display = "none";
      }
    },
    selectIcon: function(isPressed) {
      return !isPressed ? "bars" : "times";
    }
  }
};
</script>

<style scoped>
.navbar {
  width: 100vw;
  color: #fff;
  position: fixed;
  top: 0;
}

.scrolled {
  background: linear-gradient(to top, transparent 0%, rgb(0, 0, 0, 0.3) 50%);
}

.container {
  padding: 0 50px;
  height: 100px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.hamburger {
  display: none;
  font-size: 30px;
  cursor: pointer;
}

.menu2 {
  display: none;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-between;
  width: 90vw;
  background-color: #fff;
  margin: 0 auto;
  border-radius: 15px;
  color: #000;
  padding: 10px 0;
  animation: easeMenu2 1s;
}

.menu2 a {
  width: 100%;
  text-decoration: none;
  padding: 10px 0;
}

@keyframes easeMenu2 {
  0% { width: 0; } 
  100% { width: 90vw; }
}

@media screen and (max-width: 375px) {
  .container {
    padding: 0 30px;
  }

  .hamburger {
    display: block;
  }

  .menu {
    display: none;
  }
}
</style>