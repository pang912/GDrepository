<template>
  <header>
    <div class="navBar">
      <a>简易导航</a>
      <div class="navbar-collapse">
        <div class="nav-title">
          <div v-for="item in headerData">{{ item.title }}</div>
        </div>
        <div>24K导航</div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      headerData: [
        {
          title: "首页",
        },
        {
          title: "手册",
        },
        {
          title: "书籍",
        },
        {
          title: "公号",
        },
        {
          title: "脱单",
        },
        {
          title: "交流群",
        },
      ],
    };
  },
};
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

.navBar .nav-title {
  display: flex;
  justify-content: space-around;
  width: 40%;
}
</style>