<template>
  <div class="page">
    <div class="nav">
      <div class="nav-logo">
        <img src="http://www.jq22.com/demo/html520160125/images/avatar.jpg" />
      </div>
      <div class="nav-introduce">
        <h2>林间有-枫</h2>
        <p>Always believe that the good world is about to happen - feng</p>
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
    <div class="main"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      navList: [
        { id: 1, name: "关于" },
        { id: 2, name: "列表" },
        { id: 3, name: "联系" }
      ],
      index: 1
    };
  },
  methods:{
      /** 切换列表 */
      tabListItem(id){
          this.index = id
      },
  },
  mounted(){
      console.log(123);
      
  },
};
</script>

<style lang="scss">
.page {
  .nav {
    width: 300px;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background-color: #4acaa8;
    color: #d1f1e9;
    text-align: center;
    overflow: hide;
    .nav-logo {
      padding: 80px 0 30px;
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
        height: 50px;
        line-height: 50px;
        font-size: 18px;
        cursor: pointer;
        &.activer {
          background-color: #fff;
          span {
            color: #4acaa8;
          }
        }
      }
    }
  }
}
</style>
