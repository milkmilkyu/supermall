<template>
  <div class="goods-item">
    <img :src="goodsItem.show.img" alt="" />
    <div class="goods-info">
      <p>{{ goodsItem.title }}</p>
      <span class="price">{{ goodsItem.price }}</span>
      <span class="collect">{{ goodsItem.cfav }}</span>
    </div>
  </div>
</template>
<script>
export default {
  name: "GoodsListItem",
  components: {},
  props: {
    goodsItem: {
      type: Object,
      default() {
        return [];
      }
    }
  }
};
</script>
<style scoped>
.goods-item {
  position: relative;
  padding-bottom: 40px;
  width: 48%;
}
.goods-item img {
  width: 100%;
  border-radius: 5px;
}
.goods-info {
  position: absolute;
  bottom: 5px;
  left: 0;
  right: 0;
  font-size: 12px;
  text-align: center;
  overflow: hidden;
}
.goods-info p {
  margin-bottom: 3px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.goods-info .price {
  margin-right: 20px;
  color: var(--color-high-text);
}
.goods-info .collect {
  position: relative;
}
.goods-info .collect::before {
  content: "";
  position: absolute;
  left: -16px;
  top: -1px;
  background: url("~assets/img/common/collect.svg") 0 0/14px;
  width: 14px;
  height: 14px;
}
</style>
