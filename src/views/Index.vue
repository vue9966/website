<template>
  <div class="page">
    <div class="nav">
      <div class="nav-logo">
        <img src="../assets/img/top2.png" />
      </div>
      <div class="nav-introduce">
        <h2>林间有-枫</h2>
        <p>Face a new life every day - feng</p>
      </div>
      <div class="nav-list">
        <div
          :class="index==item.id ? 'nav-list-item activer':'nav-list-item'"
          v-for="(item) of navList"
          @click="tabListItem(item.id)"
          :key="item.id"
        >
          <span href="one">{{item.name}}</span>
        </div>
      </div>
    </div>
    <div class="main">
      <div class="main-banner">
        <img src="../assets/img/banner.png" alt />
      </div>
      <div class="main-box">
        <div class="main-about">
          <h1 class="title-h1">嗨，你好</h1>
          <div class="title-p">
            <p>来自于某间公司切图仔</p>
            <p>前端工程师</p>
          </div>

          <div class="about-content">
            <p>1.熟悉HTML , CSS , javascript技术;</p>
            <p>2.熟悉jQuery , Vue , Bootstrap , MUI , MintUI , Vuex等框架;</p>
            <p>3.熟悉HTML5 , CSS3 , 新特性,熟悉移动APP的开发模式能够使用媒体查询,响应式布局适配不同的设备;</p>
            <p>4.熟悉Ajax , json , jsonp , axios可以配合后台端口 , 完成前后台交互;</p>
            <p>5.熟悉CSS预处理语言less , 能够利用svn进行源代码管理;</p>
            <p>6.熟悉Session 以及Cookie会话技术;</p>
            <p>7.熟悉微信小程序开发</p>
            <p>8.高性能的页面文档流 , 规范 , 工整 , 能够提炼可服用的模块 , 注释清晰;</p>
          </div>
        </div>
        <div class="main-about">
          <div class="title-p">
            <p>问题列表</p>
            <p>平时遇到一些问题以及总结</p>
          </div>
          <div class="about-content about-problem">
            <p>平时工作中会很多很多问题</p>
            <p>要不断的百度所以我要做一下总结....</p>
            <p>加油</p>
            <span>开始问题之旅 →</span>
          </div>
        </div>
        <div class="main-about">
          <div class="title-p">
            <p>联系方式</p>
            <p>方便大家交流</p>
          </div>
          <div class="about-content about-icon">
            <p>
              <i class="iconfont icon-weixin wx"></i>
              <span>WeChat：</span>
              <span class="icon-text">vue9966</span>
            </p>
            <p>
              <i class="iconfont icon-qq qq"></i>
              <span>QQ：</span>
              <span class="icon-text">937982061</span>
            </p>
            <p>
              <i class="iconfont icon-GitHub"></i>
              <span>GitHub：</span>
              <span class="icon-text">vue9966</span>
            </p>
            <p>
              <i class="iconfont icon-youxiang youxiang"></i>
              <span>Mail：</span>
              <span class="icon-text">vue9966@163.com</span>
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navList: [
        { id: 1, name: "关于" },
        { id: 2, name: "问题" },
        { id: 3, name: "联系" }
      ],
      index: 1
    };
  },
  methods: {
    /** 切换列表 */
    tabListItem(id) {
      this.index = id;
      if (id == 3) {
        document.body.scrollTop = 900;
        window.pageYOffset = 900;
        document.documentElement.scrollTop = 900;
      } else if (id == 2) {
        document.body.scrollTop = 500;
        window.pageYOffset = 500;
        document.documentElement.scrollTop = 500;
      } else {
        document.body.scrollTop = 0;
        window.pageYOffset = 0;
        document.documentElement.scrollTop = 0;
      }
    },
    /** 滚动事件 */
    handleScroll() {
      var scrollTop =
        window.pageYOffset ||
        document.documentElement.scrollTop ||
        document.body.scrollTop;
      if (scrollTop >= 700) {
        this.index = 3;
      } else if (scrollTop >= 500) {
        this.index = 2;
      } else {
        this.index = 1;
      }
    }
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  }
};
</script>

<style lang="scss">
.page {
  width: 100%;
  overflow: hidden;
  .nav {
    width: 280px;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background-color: #4acaa8;
    color: #d1f1e9;
    text-align: center;
    overflow: hide;
    .nav-logo {
      padding: 60px 0 30px;
      img {
        width: 170px;
        height: 170px;
        border-radius: 100%;
      }
    }
    .nav-introduce {
      margin: 0 20px 40px;
      h2 {
        padding-bottom: 20px;
        color: #fff;
        font-size: 30px;
      }
      p {
        font-size: 24px;
      }
    }
    .nav-list {
      width: 100%;
      .nav-list-item {
        width: 100%;
        height: 60px;
        line-height: 60px;
        font-size: 18px;
        cursor: pointer;
        &.activer {
          background-color: #fff;
          span {
            color: #4acaa8;
          }
        }
        span {
          font-size: 18px;
          color: #fff;
        }
      }
    }
  }
  .main {
    padding-left: 280px;
    overflow: hidden;
    .main-banner {
      width: 100%;
      height: 320px;
      overflow: hidden;
      img {
        width: 100%;
      }
    }
    .main-box {
      .main-about {
        padding: 60px 100px;
        border-bottom: 5px solid rgb(244, 244, 244);
        &:last-of-type {
          border: none;
        }
        h1 {
          font-size: 68px;
          padding-bottom: 20px;
        }
        .about-content {
          color: #888;
          font-size: 18px;
          margin-top: 20px;
          p {
            line-height: 40px;
          }
        }
        .about-problem {
          cursor: pointer;
          span {
            display: inline-block;
            width: 200px;
            height: 60px;
            line-height: 60px;
            color: #fff;
            background-color: #4acaa8;
            text-align: center;
            margin: 20px 0;
            border-radius: 5px;
          }
          span:hover {
            background-color: #41a377;
          }
        }
        .about-icon {
          p {
            i {
              font-size: 26px;
              margin-right: 10px;
            }
            span {
              font-size: 22px;
            }
          }
        }
      }
    }
  }
}
</style>
