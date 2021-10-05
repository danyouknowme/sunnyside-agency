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
            <a href="#" class="text">About</a>
            <a href="#" class="text">Services</a>
            <a href="#" class="text">Projects</a>
            <a href="#" class="contact">Contact</a>
          </div>
      </div>
    </div>
    <div class="menu2">
      <a href="#" class="text2">About</a>
      <a href="#" class="text2">Services</a>
      <a href="#" class="text2">Projects</a>
      <a href="#" class="contact2">Contact</a>
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

.text {
  margin: 0 30px;
  text-decoration: none;
  color: #fff;
  border: none;
}

.text:hover {
  color: hsl(198, 62%, 26%);
  border-bottom: 1px solid #fff;
}


.contact {
  margin: 0 30px;
  text-decoration: none;
  background-color: #fff;
  padding: 15px 25px;
  border-radius: 25px;
  color: hsl(198, 62%, 26%);
  text-transform: uppercase;
  font-family: 'Fraunces', serif;
  font-size: 16px;
  border: 1px solid #fff;
}

.contact:hover {
  background-color: #22a0df;
  border: 1px solid hsl(198, 62%, 26%);
  color: #fff;
}

.hamburger {
  display: none;
  font-size: 30px;
  cursor: pointer;
}

.menu2 {
  display: none;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  width: 90vw;
  background-color: #fff;
  margin: 0 auto;
  border-radius: 15px;
  color: #000;
  padding: 10px 0;
  animation: easeMenu2 0.5s;
  z-index: 1;
}

.text2 {
  width: 95%;
  text-decoration: none;
  padding: 10px 0;
  color: hsl(198, 62%, 26%);
}

.contact2 {
  padding: 10px 0;
  margin-top: 5px;
  width: 95%;
  text-decoration: none;
  background-color: #3DBEFF;
  border-radius: 5px;
  text-transform: uppercase;
  color: #fff;
  font-family: 'Fraunces', serif;
  font-size: 16px;
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