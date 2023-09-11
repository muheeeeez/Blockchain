<template>
  <section>
    <div class="hamburger-menu" @click="onToggleMenu">
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
    </div>
  </section>
</template>

<script>
export default {
  provide() {
    return {
      menuButton: this.toggleMenu,
    };
  },
  data() {
    toggleMenu = false;
  },
  methods: {
    onToggleMenu() {
      this.toggleMenu = !this.toggleMenu;
    },
  },
};
</script>

<style scoped>
.hamburger-menu {
  display: none;
  cursor: pointer;
  background-color: #333;
  width: 30px;
  height: 20px;
  position: relative;
}
.bar {
  width: 100%;
  height: 4px;
  background-color: #fff;
  position: absolute;
  transition: transform 0.4s ease-in-out;
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
  .hamburger-menu {
    display: inline-block;
  }
}
</style>