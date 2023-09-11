<template>
  <section>
    <nav>
      <div class="nav-container">
        <div class="logo">Art.NFT</div>
        <div class="hamburger-menu" @click="onToggleMenu">
          <div class="bar"></div>
          <div class="bar"></div>
          <div class="bar"></div>
        </div>
        <div :class="{ 'menu-active': toggleMenu }">
          <ul>
            <li>Explore</li>
            <li>Markplace</li>
            <li>Blog</li>
            <li>LearnAboutBlockchain</li>
          </ul>
        </div>
        <button class="nav-button" :class="{ 'menu-active': toggleMenu }">
          Join our Community
        </button>
      </div>
    </nav>
  </section>
</template>
<script>
export default {
  data() {
    return {
      toggleMenu: false,
    };
  },
  methods: {
    onToggleMenu() {
      this.toggleMenu = !this.toggleMenu;
    },
  },
};
</script>

<style scoped>
li {
  list-style: none;
  font-size: 15px;
}
.nav-container {
  display: flex;
  margin-top: 60px;
  color: #fff;
  align-items: center;
  justify-content: space-around;
}
nav ul {
  display: flex;
}
nav li {
  margin: 0 60px 0 0;
  justify-content: space-evenly;
}
nav .logo {
  margin-left: 45px;
  font-size: 50px;
}
.nav-button {
  background-color: transparent;
  border-radius: 28px;
  border: 1px solid #fff;
  cursor: pointer;
  color: #fff;
  font-size: 17px;
  padding: 16px 31px;
}
.menu-active ul,
.menu-active {
  display: block;
}
.menu-active li {
  font-size: 20px;
  margin: 75px 0 0 0;
  z-index: 1;
}

.hamburger-menu {
  display: none;
  cursor: pointer;
  background-color: blue;
  width: 30px;
  height: 20px;
  position: relative;
}
.bar {
  width: 100%;
  height: 4px;
  background-color: #fff;
  position: absolute;
  transition: transform 1.4s ease-in-out;
}
.bar:nth-child(1) {
  top: 0;
}

.bar:nth-child(2) {
  top: 8px;
}

.bar:nth-child(3) {
  top: 16px;
}
.hamburger-menu.open .bar:nth-child(1) {
  transform: translateY(8px) rotate(-45deg);
}

.hamburger-menu.open .bar:nth-child(2) {
  opacity: 0;
}

.hamburger-menu.open .bar:nth-child(3) {
  transform: translateY(-8px) rotate(45deg);
}
@media screen and (min-width: 414px) and (max-width: 1200px) {
  nav ul {
    display: none;
  }
  nav button {
    display: none;
  }
  .hamburger-menu {
    display: inline-block;
  }
}
</style>