<template>
  <div class="nav-bar-wrapper">
    <div class="container">
      <router-link class="logo" to="/" tag="div"></router-link>
      <ul class="nav-item-list">
        <router-link class="nav-item" to="/block" tag="li" active-class="choosed">Blocks</router-link>
        <router-link class="nav-item" to="/extrinsic" tag="li" active-class="choosed">Extrinsics</router-link>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: "NavBar",
  data() {
    return {
      navSelected: ""
    };
  },
  methods: {
    changeLanguage(language) {
      GLOBAL.vbus.$emit("CHANGE_LANGUAGE", language);
      this.$store.dispatch("SetLanguage", language);
    }
  }
};
</script>
<style lang="scss" scoped>
.nav-bar-wrapper {
  height: 70px;
  background-color: #333748;
  position: relative;
  .container {
    display: flex;
    align-items: center;
    height: 100%;
    .logo {
      height: 100%;
      width: 200px;
      background: url("../../assets/images/logo.png") no-repeat left center;
      background-size: 140px auto;
      cursor: pointer;
    }
    .nav-item-list {
      display: flex;
      align-items: center;
      .nav-item {
        height: 70px;
        line-height: 70px;
        cursor: pointer;
        font-size: 16px;
        transition: color 0.3s;
        user-select: none;
        color: #9fa4b8;
        &:not(:last-child) {
          margin-right: 30px;
        }
        &:hover {
          color: #fff;
        }
        &.choosed {
          color: #fff;
        }
      }
    }
  }
}
</style>
