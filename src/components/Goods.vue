<template>
    <div class="goods" >
      <img :src="a.imagePath" />
      <div class="text">{{ a.name }}</div>
      <div class="cart">
        <div class="price">￥{{ a.price }}</div>
        <img src="../assets/cart.png" />
      </div>
    </div>
</template>

<script>
export default {
  props: ["a"],
};
</script>

<style lang="scss" scoped>
.goods {
  width: 150px;
  height: 190px;
  border: 1px solid;
  background-color: white;
  flex-shrink: 1;
  margin-top: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  > img {
    width: 100px;
    height: 100px;
    cursor: pointer;
  }
  > .text {
    padding: 5px;
    width: 100%;
    height: 25px;
    font-size: 10px;
    overflow: hidden;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    text-overflow: ellipsis;
    pointer-events: initial;
    cursor: pointer;
  }
  .cart {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
    > img {
      width: 30px;
      height: 30px;
    }
    > .price {
      color: #eaa65a;
    }
  }
}

</style>