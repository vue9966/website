<template>
  <div class="home">
    <!-- LOGO -->
    <div class="home-logo">
      <img src=".././assets/logo.jpg" alt />
    </div>
    <!-- LOGO  end-->

    <div class="home-title">林间-枫</div>
    <div class="home-introduce">{{introduceNmae}}</div>
    <div class="home-start" @click="openIndex">开始你的旅行 →</div>
    <div class="home-features flex">
      <div class="home-features-list" v-for="(item,index) of list" :key="index">
        <h2>{{item.title}}</h2>
        <p>{{item.contern}}</p>
      </div>
    </div>
    <div class="home-foot">来自本人纯属于吹水</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      introduceNmae: "来自林间-枫的个人博客",
      list: [
        {
          id: 1,
          title: "个人介绍",
          contern:
            "来自某间小公司的前端小菜鸡，懂JS,HTML,CSS,Vue等前端技术，了解后端PHP,Mysql,只是懂一点皮毛哦,不要太当回事，哈哈"
        },
        {
          id: 2,
          title: "为什么写博客？",
          contern:
            "只是为了玩一下记录一些好玩的技术吧，以后不用老是百度啦，自己查看一下个人博客，最后：也是记录我转行,加油！！"
        },
        {
          id: 3,
          title: "个人爱好",
          contern:
            "喜欢游泳跑步，旅游等，喜欢撸猫，交朋友(女性那种的哦)，哈哈，（开始你博客的旅行吧）"
        }
      ]
    };
  },
  methods: {
    /** 字体效果 */
    // startNmae() {
    //   this.introduceNmae = "";
    //   var index = 0;
    //   var introduce = "来自林间-枫的个人博客";
    //   var clearIn = setInterval(() => {
    //     this.introduceNmae += introduce.charAt(index);
    //     if (index++ === introduce.length) {
    //       clearInterval(clearIn);
    //     }
    //   }, 200);
    // },
    /** 打开首页 */
    openIndex() {
      this.$router.push("/index");
    }
  },
  mounted() {
    this.startNmae();
    console.log(this.title);
  }
};
</script>

<style lang="scss"  scoped>
.home {
  max-width: 960px;
  margin: 0 auto;
  text-align: center;
  position: relative;
  .home-logo {
    margin-top: 40px;
  }
  .home-title {
    font-weight: bold;
    margin: 40px 0;
    font-size: 36px;
    color: #2c3e50;
    font-family: "-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Oxygen,Ubuntu,Cantarell,Fira Sans,Droid Sans,Helvetica Neue,sans-serif";
  }
  .home-introduce {
    font-size: 24px;
    color: #6a8bad;
    margin: 45px 0;
  }
  .home-start {
    display: inline-block;
    height: 60px;
    line-height: 60px;
    color: #fff;
    background-color: #3eaf7c;
    border-radius: 5px;
    margin: 0 auto;
    font-size: 16px;
    cursor: pointer;
    padding: 0 30px;
  }
  .home-start:hover {
    background-color: #41a377;
  }
  .home-features {
    margin: 40px 0;
    border-top: 1px solid #6a8bad;
    justify-content: space-between;

    .home-features-list {
      flex-grow: 1;
      flex-basis: 30%;
      max-width: 30%;
      text-align: left;
      padding-top: 20px;
      h2 {
        font-weight: 500;
        color: #3a5169;
      }
      p {
        margin: 0;

        color: #4e6e8e;
        line-height: 35px;
      }
    }
  }
  .home-foot {
    color: #ccc;
    position: fixed;
    bottom: 20px;
    left: 50%;
    transform: translate(-50%,-50%);
  }
}
</style>
