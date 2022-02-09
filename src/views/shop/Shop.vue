<template>
  <div class="wrapper">
    <div class="search">
      <div
        class="search__back iconfont"
        @click="handleBackClick"
      >&#xe679;</div>
      <div class="search__content">
        <span class="search__content__icon iconfont">&#xe6ac;</span>
        <input
          class="search__content__input"
          placeholder="请输入商品名称搜索"
        />
      </div>
    </div>
    <ShopInfo :item="data.item" :hideBorder="true"/>
  </div>
</template>

<script>
import { reactive } from 'vue'
import { useRouter } from 'vue-router'
import { get } from '../../utils/request'
import ShopInfo from '../../components/ShopInfo'

export default {
  name: 'Shop',
  components: { ShopInfo },
  setup () {
    const router = useRouter()
    const data = reactive({ item: {} })
    const getItemData = async () => {
      const result = await get('/api/shop/1')
      if (result?.errno === 0 && result?.data) {
        data.item = result.data
      }
      console.log(result)
    }
    getItemData()
    const handleBackClick = () => {
      router.back()
    }
    return { data, handleBackClick }
  }
}
</script>

<style lang="scss" scoped>
@import '../../style/viriables.scss';
.wrapper {
  padding: 0 .18rem
}
.search {
  display: flex;
  margin: .14rem 0 .04rem 0;
  line-height: .32rem;
  &__back {
    width: .32rem;
    font-size: .2rem;
  }
  &__content {
    display: flex;
    flex: 1;
    background: $search-bgColor;
    border-radius: .16rem;
    &__icon {
      width: .44rem;
      text-align: center;
      font-size: .18rem;
      color: $search-fontColor;
    }
    &__input {
      display: block;
      width: 100%;
      padding-right: .2rem;
      border: none;
      outline: none;
      background: none;
      color: $content-fontcolor;
      &::placeholder {
        color: $content-fontcolor;
      }
    }
  }
}

</style>
