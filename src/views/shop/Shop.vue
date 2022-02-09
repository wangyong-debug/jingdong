<template>
  <div class="wrapper">
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
      name: '沃尔玛'
    }
    return { item }
  }
}
</script>

<style lang="scss" scoped>
.wrapper {
  padding: 0 .18rem
}

</style>
