<template>
  <div>
    <div class="wrapper">
      <StaticPart />
      <Nearby />
  </div>
    <Docker />
  </div>
</template>

<script>
import StaticPart from './StaticPart'
import Nearby from './Nearby'
import Docker from './Docker'

export default {
  name: 'Home',
  components: { StaticPart, Nearby, Docker }
}
</script>

<style lang="scss" scoped>
.wrapper{
  overflow-y: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom:.5rem;
  right: 0;
  padding: 0 .18rem .3rem .1rem;
}
</style>
