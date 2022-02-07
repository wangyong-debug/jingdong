<template>
  <div class="position">
    <span class="iconfont position__icon">&#xe7f1;</span>
    西安邮电大学东区安悦公寓北楼
    <span class="iconfont position__notice">&#xe7c4;</span>
  </div>
  <div class="search">
    <span class="iconfont">&#xe6ac;</span>
    <input class="search__text" placeholder="山姆商店优惠商品" />
  </div>
  <div class="banner">
    <img
      class="banner__img"
      src="http://www.dell-lee.com/imgs/vue3/banner.jpg"
    />
  </div>
  <div class="icons">
    <div
      v-for="item in iconList"
      :key="item.id"
      class="icons__item"
    >
      <img class="icons__item__img"
      :src="item.iconUrl"
      >
      <p class="icons__item__desc">{{item.icontext}}</p>
    </div>
  </div>
  <div class="gap"></div>
</template>

<script>
export default {
  name: ' StaticPart ',
  setup () {
    const iconList = [{
      id: 1,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/超市.png',
      icontext: '超市便利'
    }, {
      id: 2,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/菜市场.png',
      icontext: '菜市场'
    }, {
      id: 3,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/水果店.png',
      icontext: '水果店'
    }, {
      id: 4,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/鲜花.png',
      icontext: '鲜花绿植'
    }, {
      id: 5,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/医药健康.png',
      icontext: '医药健康'
    }, {
      id: 6,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/家居.png',
      icontext: '家居时尚'
    }, {
      id: 7,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/蛋糕.png',
      icontext: '烘培蛋糕'
    }, {
      id: 8,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/签到.png',
      icontext: '签到'
    }, {
      id: 9,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/大牌免运.png',
      icontext: '大牌免运'
    }, {
      id: 10,
      iconUrl: 'http://www.dell-lee.com/imgs/vue3/红包.png',
      icontext: '红包套餐'
    }]
    return { iconList }
  }
}
</script>

<style lang="scss" scoped>
@import "../../style/viriables.scss";
@import "../../style/mixins.scss";
.position {
  overflow: hidden;
  position: relative;
  padding: 0.16rem 0.24rem 0.16rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  @include ellipsis;
  .position__icon {
    position: relative;
    top: 0.01rem;
    font-size: 0.2rem;
  }
  .position__notice {
    position: absolute;
    right: 0;
    top: 0.17rem;
    font-size: 0.2rem;
  }
  color: $content-fontcolor;
}
.search {
  margin-bottom: 0.12rem;
  line-height: 0.32rem;
  background: #f5f5f5;
  color: #b7b7b7;
  border-radius: 0.16rem;
  .iconfont {
    display: inline-block;
    padding: 0 0.12rem 0 0.16rem;
    font-size: 0.16rem;
  }
  &__text {
    display: inline-block;
    width: 80%;
    font-size: 0.14rem;
    background-color: transparent;
    border: 0;
  }
}
.banner {
  height: 0;
  overflow: hidden;
  padding-bottom: 25.4%;
  &__img {
    width: 100%;
  }
}
.icons {
  display: flex;
  flex-wrap: wrap;
  margin-top: 0.16rem;
  &__item {
    width: 20%;
    &__img {
      display: block;
      width: 0.4rem;
      height: 0.4rem;
      margin: 0 auto;
    }
    &__desc {
      margin: 0.06rem 0 0.06rem 0;
      text-align: center;
      color: $content-fontcolor;
    }
  }
}
.gap {
  margin: 0 -0.18rem;
  height: 0.1rem;
  background: $content-bgColor;
}
</style>
