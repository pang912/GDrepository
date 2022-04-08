<template>
  <div>
    <SideBar></SideBar>
    <div class="content">
      <section>
        <!-- 分类 -->
        <div class="category">
          <span>图书类</span>
        </div>
        <!-- 导航链接列表 -->
        <ul class="linkList">
          <!-- 链接项 -->
          <li class="linkNodes" v-for="item in requestData.data">
            <div class="remoteAddress" @click="openLink(item)">
              <div>
                <!-- 链接图标 -->
                <img src="../../assets/x_cd-cover.png" alt="" />
              </div>
              <div>
                 <!-- 链接标题 -->
                <div style="font-size: 16px; text-align: start">
                  {{ item.title }}
                </div>
                <!-- 链接描述 -->
                <div class="linkDes" :title="item.description">
                  {{ item.description }}
                </div>
              </div>
            </div>
          </li>
        </ul>
      </section>
    </div>
  </div>
</template>


<script>
import SideBar from "./sideBar.vue";
export default {
  components: {
    SideBar,
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
            description:
              "这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍这是一段介绍",
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
  margin-bottom: 20px;
}

.linkNodes {
  width: 25%;
  margin-bottom: 15px;
  padding: 5px 10px;
  list-style-type: none;
}

.linkNodes :hover {
  box-shadow: 0px 0px 20px 5px #ccc;
  transition: all 1s;
}

.linkNodes .remoteAddress {
  display: flex;
  height: 110px;
  color: #000;
  cursor: pointer;
  color: #ee9a49;
  padding: 5px 10px;
  border: 1px solid #ccc;
}

.linkNodes .remoteAddress :hover {
  box-shadow: none;
}

.linkNodes .remoteAddress > div:nth-child(1) {
  width: 20%;
}

.linkNodes .remoteAddress > div:nth-child(2) {
  padding-left: 10px;
}

.linkDes {
  font-size: 12px;
  width: 235px;
  height: 80px;
  text-overflow: ellipsis;
  overflow: hidden;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 5;
  text-align: start;
}

@media only screen and (max-width: 1600px) {
  .content {
    margin: 10px 50px;
    width: auto;
  }
}

@media only screen and (max-width: 1492px) {
  .linkDes {
    width: 100%;
  }
  .linkNodes .remoteAddress > div:nth-child(1) {
    width: 17%;
  }
}

@media only screen and (max-width: 1250px) {
  .linkNodes .remoteAddress > div:nth-child(1) {
    width: 20%;
  }
}

@media only screen and (max-width: 1130px) {
  .linkNodes .remoteAddress > div:nth-child(1) {
    width: 28%;
  }
}

@media only screen and (max-width: 890px) {
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