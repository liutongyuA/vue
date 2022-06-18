<template>
  <div class="goodsList">
    <template v-if="!lists.length == 0">
    <Goods v-for="(i,index) in lists" :key="index" :a="i"></Goods>
    </template>
    <div class="loading" v-else>
      <img src="../assets/loading.png" alt="" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Goods from "@/components/Goods";
export default {
  data() {
    return {
      lists: [],
    };
  },
  created() {
    axios
      .post("http://152.136.246.239:3052/api/getMerchandise", {})
      .then((value) => {
        this.lists = value.data.data;
      });
  },
  components: { Goods },
};
</script>

<style lang="scss" scoped>
.goodsList {
  width: 100%;
  height: 75vh;
  overflow-y: scroll;
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  background-color: #f9f9f9;
  &::after {
    content: "";
    width: 150px;
  }
  > .loading {
    position: absolute;
    > img {
      width: 100px;
      height: 100px;
      margin: 50px auto;
    }
  }
}
</style>