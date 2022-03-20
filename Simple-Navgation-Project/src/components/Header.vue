<template>
  <header>
    <div class="navBar">
      <a>简易导航</a>
      <div class="navbar-collapse">
        <div>111</div>
        <div>222</div>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
header {
  background: #3d4557;
  height: 55px;
  color: #fff;
  line-height: 55px;
}
.navBar {
  display: flex;
  justify-content: start;
  width: 92%;
  margin: 0 auto;
}
.navBar a {
  display: flex;
  width: 10%;
  padding-left: 20px;
}

.navBar .navbar-collapse {
  display: flex;
  justify-content: space-between;
  width: 90%;
}
</style>