<template>
  <div class="search">
    <!-- 搜索引擎 -->
    <ul class="search-engine">
      <li v-for="item in list" @click="engineChange($event, item)">
        {{ item.title }}
      </li>
    </ul>
    <!-- 搜索栏 -->
    <div class="search-input">
      <!-- 引擎名称 -->
      <div class="engine-name">
        <img src="../../assets/x_wave.png" alt="" />
        {{ title }}
      </div>
      <!-- 搜索输入框 -->
      <input type="text" :placeholder="description" />
      <!-- 搜索按钮 -->
      <button>搜索</button>
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
    let li1 = document.querySelector(".search-engine li");
    li1.classList.add("selected");
  },
  methods: {
    engineChange(e, i) {
      console.log(e, i);
      let li = document.querySelectorAll(".search-engine li");
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
  display: flex;
  flex-flow: column;
  width: 1500px;
  background: #fff;
  margin: 10px auto;
  padding: 18px;
  border-radius: 10px;
}

.search-engine {
  display: flex;
  justify-content: space-around;
  margin: 10px auto;
  margin-top: 0;
  width: 80%;
}

.search-engine li {
  list-style-type: none;
  color: #999;
  font-size: 15px;
  cursor: pointer;
}

.search-engine .selected {
  border-bottom: 2px solid #000;
  color: #000;
}

.search-input {
  display: flex;
  justify-content: center;
  position: relative;
  margin: 0 auto;
  width: 80%;
}

.engine-name {
  width: 80px;
  border: 1px solid #e9ecef;
  border-top-left-radius: 0.25rem;
  border-bottom-left-radius: 0.25rem;
  cursor: pointer;
}

.engine-name:hover {
  background: #ced4da;
}

.search-input img {
  width: 20px;
  vertical-align: text-top;
}

.search-input input {
  width: calc(100% - 80px);
  padding: 5px 0 5px 10px;
  border: 1px solid #ced4da;
  border-radius: 0 5px 5px 0;
  outline: none;
}

.search-input input:focus {
  color: #495057;
  background-color: #fff;
  border-color: #4788cf;
  box-shadow: 0 0 0 0.2rem rgb(31 73 119 / 25%);
}

.search-input button {
  position: absolute;
  right: 0px;
  width: 60px;
  height: 100%;
  outline: none;
  border: 0;
  border-radius: 0 5px 5px 0;
  cursor: pointer;
  background: #e9ecef;
}

.search-input button:hover {
  background: #ced4da;
}

@media only screen and (max-width: 1600px) {
  .search {
    margin: 10px 50px;
    width: auto;
  }
}
</style>