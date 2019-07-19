<template>
  <div class="footer-bar">
    <div class="container content">©2019 Vue Spa. All rights reserved</div>
  </div>
</template>

<script>
export default {
  name: "FooterBar"
};
</script>

<style lang='scss' scoped>
.footer-bar {
  .content {
    font-size: 14px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #262628;
    color: #fff;
    height: 50px;
    width: 100%;
  }
}
</style>