<template>
  <div>
    <Search></Search>
    <div class="content">
      <section>
        <div class="category">
          <span>图书类</span>
        </div>
        <ul class="linkList">
          <li v-for="item in requestData.data" class="linkNodes">
            <div class="remoteAddress" @click="openLink(item)">
              <div style="width: 20%">
                <img src="../../public/favicon.ico" alt="" />
              </div>
              <div style="padding-left: 10px">
                <div style="font-size: 16px">{{ item.title }}</div>
                <div style="font-size: 12px">{{ item.description }}</div>
              </div>
            </div>
          </li>
        </ul>
      </section>
    </div>
  </div>
</template>


<script>
import Search from "./Search.vue";
export default {
  components: {
    Search,
  },
  data() {
    return {
      requestData: {
        err_no: 0,
        traceId: "00000000000",
        err_message: "success",
        total: 100,
        data: [
          {
            title: "百度首页",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "百度首页",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
          {
            title: "这是一个标题",
            description: "这是一段介绍",
            remoteLink: "https://www.baidu.com",
            iconSrc:
              "https://img0.baidu.com/it/u=2299005931,568974025&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=500",
          },
        ],
      },
    };
  },
  methods: {
    openLink(item) {
      console.log(item);
      window.open(item.remoteLink, "_blank");
    },
  },
};
</script>

<style scoped>
.content {
  box-sizing: border-box;
  display: flex;
  flex-flow: column;
  width: 1500px;
  background: #fff;
  margin: 10px auto;
  padding: 18px;
  border-radius: 10px;
}

.content .category {
  display: flex;
  justify-content: start;
  font-size: 16px;
  margin-bottom: 20px;
  padding-bottom: 10px;
  border-bottom: 1px solid #ccc;
}

.linkList {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  margin-bottom: 20px;
}
.linkNodes {
  box-sizing: border-box;
  width: 12.5%;
  margin-bottom: 15px;
  padding: 5px 10px;
  list-style-type: none;
}

.linkNodes :hover {
  box-shadow: 10px 10px 10px #ccc;
}

.linkNodes .remoteAddress {
  display: flex;
  color: #000;
  cursor: pointer;
  color: #ee9a49;
  padding: 5px 10px;
  border: 1px solid #ccc;
}

.linkNodes .remoteAddress :hover {
  box-shadow: none;
}

@media only screen and (max-width: 1533px) {
  .linkNodes {
    width: 25%;
  }
}

@media only screen and (max-width: 1600px) {
  .content {
    margin: 10px 50px;
    width: auto;
  }
}

@media only screen and (max-width: 835px) {
  .linkNodes {
    width: 50%;
  }
}

@media only screen and (max-width: 500px) {
  .linkNodes {
    width: 100%;
  }
}
</style>