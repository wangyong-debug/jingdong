<template>
  <div>
    <div class="wrapper">
      <div class="position">
        <span class="iconfont position__icon">&#xe7f1;</span>
        西安邮电大学东区安悦公寓北楼西安邮电大学东区安悦公寓北楼
        <span class="iconfont position__notice">&#xe7c4;</span>
      </div>
    </div>
    <div class="docker">
      <div class="docker__item docker__item--active">
        <div class="iconfont">&#xe6b8;</div>
        <div class="docker__title">首页</div>
      </div>
      <div class="docker__item">
        <div class="iconfont">&#xe600;</div>
        <div class="docker__title">购物车</div>
      </div>
      <div class="docker__item">
        <div class="iconfont">&#xe60e;</div>
        <div class="docker__title">订单</div>
      </div>
      <div class="docker__item">
        <div class="iconfont">&#xe78b;</div>
        <div class="docker__title">我的</div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.wrapper{
  position: absolute;
  top: 0;
  left: 0;
  bottom:.5rem;
  right: 0;
  padding: 0 .18rem;
}
.position{
  overflow: hidden;
  position: relative;
  padding: .16rem .24rem .16rem 0;
  line-height: .22rem;
  font-size: .16rem;
  white-space: nowrap;
  text-overflow: ellipsis;
  .position__icon{
    position: relative;
    top: .01rem;
    font-size: .2rem;
  }
  .position__notice{
    position: absolute;
    right: 0;
    top: .17rem;
    font-size: .2rem;
  }
}
.docker{
  display: flex;
  box-sizing: border-box;
  position: absolute;
  padding: 0 .18rem;
  left: 0;
  bottom: 0;
  width: 100%;
  height: .49rem;
  border-top: .01px solid #f1f1f1;
  &__item{
    flex:1;
    text-align: center;
    .iconfont{
      margin:.07rem 0 .02rem 0;
      font-size: .18rem;
    }
    &--active{
      color: #1fa4fc;
    }
  }
  &__title{
    font-size: .2rem;
    transform: scale(.5,.5);
    transform-origin: center top;
}
}

</style>
