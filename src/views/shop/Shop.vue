<template>
  <div class="wrapper">
    <div class="search">
      <div class="search__back iconfont">&#xe679;</div>
      <div class="search__content">
        <span class="search__content__icon iconfont">&#xe6ac;</span>
        <input class="search__content__input">
      </div>
    </div>
    <ShopInfo :item="item" :hideBorder="true"/>
  </div>
</template>

<script>
import ShopInfo from '../../components/ShopInfo'

export default {
  name: 'Shop',
  components: { ShopInfo },
  setup () {
    const item = {
      _id: '1',
      name: '沃尔玛',
      imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
      sales: 1000,
      exprressLimit: 0,
      expressPrice: 5,
      slogan: 'VIP尊享89元减4元运费券'
    }
    return { item }
  }
}
</script>

<style lang="scss" scoped>
.wrapper {
  padding: 0 .18rem
}
.search {
  display: flex;
  margin: .2rem 0 .16rem 0;
  line-height: .32rem;
  &__back {
    width: .32rem;
    font-size: .2rem;
  }
  &__content {
    display: flex;
    flex: 1;
    background: #f5f5f5;
    border-radius: .16rem;
    &__icon {
      width: .44rem;
      height: .32rem;
      font-size: .18rem;
    }
    &__input {
      display: block;
      width: 100%;
      padding-right: .2rem;
      border: none;
      outline: none;
      background: none;
    }
  }
}

</style>
