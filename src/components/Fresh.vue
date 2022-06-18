<template>
  <div class="fresh">
    <div class="nav">
      <div class="leftIcon">
        <i class="iconfont icon-xiangzuo_o"></i>
      </div>
      <span>京东生鲜</span>
      <div class="rightIcon">
        <i class="iconfont icon-gouwuche"></i>
        <i class="iconfont icon-gengduo"></i>
      </div>
    </div>
    <div class="tab">
      <ul>
        <li>精选</li>
        <li class="active">水果</li>
        <li>海鲜</li>
        <li>肉禽蛋</li>
      </ul>
    </div>
    <GoodsList></GoodsList>
    <div class="footer">
      <img src="../assets/sy.jpg" />
      <img src="../assets/fl.jpg" />
      <img src="../assets/sccx.jpg" />
      <img src="../assets/rmph.jpg" />
      <img src="../assets/yx100.jpg" />
    </div>
  </div>
</template>

<script>
import GoodsList from "@/components/GoodsList";
export default {
  components: { GoodsList },
};
</script>

<style lang="scss" scoped>
.fresh {
  width: 400px;
  display: flex;
  flex-direction: column;
  align-items: center;
  > .nav {
    width: 100%;
    height: 50px;
    border-bottom: 1px solid #eee;
    display: flex;
    justify-content: space-between;
    align-items: center;
    > span {
      font-size: 27px;
      font-weight: bold;
      color: red;
    }
    .iconfont {
      font-size: 25px;
    }
  }
  > .tab {
    width: 100%;
    > ul {
      margin: 5px 23px;
      height: 40px;
      line-height: 40px;
      font-size: 14px;
      display: flex;
      justify-content: space-between;
      li {
        padding: 0 10px;
        position: relative;
        &.active {
          font-weight: bold;
        }
      }
      .active::before {
        content: "";
        position: absolute;
        width: 100%;
        bottom: 0;
        left: 0;
        border-bottom: 3px solid;
      }
    }
  }
  .footer {
    width: 100%;
    height: 40px;
    display: flex;
    justify-content: space-between;
    > img {
      width: 45px;
      height: 40px;
      cursor: pointer;
    }
  }
}
</style>