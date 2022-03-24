<template>
  <header>
    <div class="navBar">
      <a class="nav-one">简易导航</a>
      <div class="navbar-collapse">
        <div class="nav-link">
          <div v-for="item in headerData">
            <a href="#">{{ item.title }}</a>
          </div>
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
.navBar .nav-one {
  display: flex;
  width: 10%;
  padding-left: 20px;
}

.navBar .navbar-collapse {
  display: flex;
  justify-content: space-between;
  width: 85%;
}

.navbar-collapse > div:nth-child(2):hover {
  font-weight: bold;
}

.navBar .nav-link {
  display: flex;
  justify-content: space-around;
  width: 400px;
}

.nav-link div {
  position: relative;
}

.nav-link div:hover {
  font-weight: bold;
}

.nav-link div a {
  text-decoration: none;
  color: #fff;
  padding: 12.46px 14px;
}

.nav-link div a::before {
  content: "";
  position: absolute;
  left: 50%;
  bottom: 2px;
  width: 0%;
  height: 2px;
  background: #db6c4a;
  transition: all 0.3s;
}

.nav-link div a:hover::before {
  width: 100%;
  left: 0;
  right: 0;
}
</style>