<template>
  <div class="mainContainer">
    <div class="sideBar">
      {{ model }}
      <sidebar />
    </div>
    <div class="main">
      <header class="header">
        <div class="left">
          <p>Jeans</p>
        </div>
        <div class="right">
          <i class="fas fa-cart-shopping"></i>
          <i class="fas fa-magnifying-glass"></i>
        </div>
      </header>
      <mainContent />
      <storeCheck />
    </div>
  </div>


</template>

<script>
import model from '../src/assets/chr_F13.glb?url'
export default {
  components: { model }
}
</script>

<style lang="scss" scoped>
.mainContainer {
  width: 90%;
  display: grid;
  grid-template-columns: 30% 70%;
  grid-template-rows: auto;
  justify-content: center;

  .main {
    .header {
      display: flex;
      padding: 30px 15px 30px 15px;
      justify-content: space-between;

      .left {
        float: left;

        p {
          font-size: 25px;
        }
      }

      .right {
        display: flex;
        float: right;
        justify-content: center;

        i {
          padding-left: 15px;
          font-size: 20px;
        }
      }
    }
  }
}
</style>