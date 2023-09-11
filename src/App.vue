<template>
  <section>
    <div>
      <the-header></the-header>
    </div>

    <div class="grid-image-container">
      <div class="image-text">
        <h2>
          Step into the world of blockchain where innovation meets opportunity.
        </h2>
      </div>
    </div>

    <div class="image-wrapper">
      <img src="images/ball.jpg" alt="" class="image" />
    </div>
    <div class="grid-button-container">
      <button class="myButton2">Explore MarketPlace</button>
      <hr class="horizontal-line" />
      <p class="paragraph-container">
        The world of blockchain is a place where innovation meets opportunity.
        Whether you're a developer, entrepreneur, or investor, blockchain offer
        endless opportunites to innovate, disrupt, and make a difference
      </p>
    </div>
    <div class="grid-container">
      <p class="grid-items">EXPERIENCETHEPOWEROFBLOCKCHAIN-THEFUTUREISNOW.</p>
      <p class="grid-items container-items">
        JOINTHEBLOCKCHAINREVOLUTION ANDUNLOCKAWORLDOFPOSSIBLITES.
      </p>
    </div>
  </section>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";

export default {
  components: { TheHeader },
};
</script>

<style>
body,
ul,
li {
  margin: 0;
  padding: 0;
  list-style: none;
  background-color: black;
  font-family: sans-serif;
  color: #fff;
}
.grid-image-container {
  margin: 0 0 0 240px;
}
.image {
  position: absolute;
  transform: translate(120%, -50%);
  z-index: -2;
  width: 40%;
}
.image-text {
  color: #fff;
  width: 63%;
  font-size: 85px;
  z-index: 1;
}
.grid-button-container {
  margin: 410px 0 0 240px;
  display: flex;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0;
  z-index: 1;
  align-items: center;
  width: 70%;
}
.myButton2 {
  background-color: rgb(107, 221, 89);
  border-radius: 48px;
  cursor: pointer;
  color: black;
  font-size: 30px;
  margin: 60px 0;
  padding: 25px;
  z-index: 1;
}
.horizontal-line {
  border: none;
  height: 2px;
  width: 15%;
  background-color: #fff;
  z-index: 1;
}
.paragraph-container {
  font-size: 22px;
  z-index: 1;
  width: 41%;
  padding: 0 160px 0 0;
}
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 65px;
  width: 75%;
  margin: 0 0 0 240px;
  font-size: 20px;
}
.grid-item {
  padding: 25px;
  border: 1px solid #ccc;
}
.container-items {
  padding-right: 100px;
  text-align: end;
}
@media screen and (min-width: 414px) and (max-width: 1200px) {
  .image {
    display: none;
  }
  .image-text {
    display: flex;
    flex-wrap: wrap;
    font-size: 90px;
    width: fit-content;
  }
  .grid-button-container {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    /* grid-template-columns: 500px 0px 650px; */
    margin: 0 auto;
  }
  .horizontal-line {
    width: 95%;
  }
  .paragraph-container{
    width: 92%;
    padding: 0 0 0 40px;
    text-align: center;
    font-size: 28px;
  }
  .grid-container {
    margin: 0 auto;
    /* font-size: 35px; */
    gap: 10px;
  }
}
</style>