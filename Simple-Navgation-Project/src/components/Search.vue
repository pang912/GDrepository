<template>
  <div class="search">
    <ul class="search-list">
      <li v-for="item in list" @click="engineChange($event, item)">
        {{ item.title }}
      </li>
    </ul>
    <div class="search-nav">
      <div class="search-toggle-btn">
        <img src="../../public/favicon.ico" alt="" />
        {{ title }}
      </div>
      <input type="text" :placeholder="description" />
      <!-- <div class="search-btn"> -->
      <button class="icon-search"></button>
      <!-- </div> -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "百度",
      description: "百度一下，你就知道",
      list: [
        {
          title: "百度",
          description: "百度一下，你就知道",
        },
        {
          title: "编程",
          description: "专注于程序员编程的搜索",
        },
        {
          title: "必应",
          description: "必应搜索",
        },
        {
          title: "微信",
          description: "微信文章搜索",
        },
        {
          title: "知乎",
          description: "知乎文章搜索",
        },
        {
          title: "谷歌",
          description: "Google搜索",
        },
      ],
    };
  },
  mounted() {
    let li1 = document.querySelector(".search-list li");
    li1.classList.add("selected");
  },
  methods: {
    engineChange(e, i) {
      console.log(e, i);
      let li = document.querySelectorAll(".search-list li");
      li.forEach((i) => {
        i.classList.remove("selected");
      });
      e.target.classList.add("selected");
      this.title = i.title;
      this.description = i.description;
    },
  },
};
</script>

<style scoped>
.search {
  box-sizing: border-box;
  display: flex;
  flex-flow: column;
  width: 1500px;
  background: #fff;
  margin: 10px auto;
  padding: 18px;
  border-radius: 10px;
}

.search-list {
  display: flex;
  justify-content: space-around;
  margin: 10px auto;
  margin-top: 0;
  width: 80%;
}

.search-list li {
  list-style-type: none;
  color: #999;
  font-size: 15px;
  cursor: pointer;
}

.search-list .selected {
  border-bottom: 2px solid #000;
  color: #000;
}

.search-nav {
  display: flex;
  justify-content: start;
  position: relative;
  margin: 0 auto;
  width: 80%;
}

.search-toggle-btn {
  width: 9%;
  border: 1px solid #ced4da;
  border-top-left-radius: 0.25rem;
  border-bottom-left-radius: 0.25rem;
  cursor: pointer;
}

.search-toggle-btn :hover {
  background: #fff;
}

.search-nav img {
  width: 20px;
  vertical-align: text-top;
}

.search-nav input {
  width: 100%;
  padding: 5px;
  box-sizing: border-box;
  border: 1px solid #ced4da;
  outline: none;
}

.search-nav button {
  outline: none;
  border: 0;
}

.icon-search {
  background: url(../../public/favicon.ico) no-repeat;
  background-size: 22px 22px;
  width: 27px;
  height: 27px;
  /* padding-top: 5px; */
}

@media only screen and (max-width: 1600px) {
  .search {
    margin: 10px 50px;
    width: auto;
  }
}
</style>