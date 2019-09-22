<template>
  <header>
      <!-- 顶部通栏 start -->
      <div class="top-wrap">
        <div class="back">
          <i class="icon-arrow_lift"></i>
        </div>
        <div class="search-box">
          <i></i>
          <input type="text" placeholder="搜索店内商品">
        </div>
        <div class="share-box">
          <a href="#" class="pinon">
            <span>拼单</span>
          </a>
          <a href="#" class="share">
            <i class="circle"></i>
            <i class="circle"></i>
            <i class="circle"></i>
          </a>
        </div>
      </div>
      <!-- 顶部通栏 end -->

      <!-- 商户主体 start -->
      <div class="contain-wrap"></div>
      <!-- 商户主体 end -->

      <!-- 底部优惠 start -->
      <div class="bottom-wrap"></div>
      <!-- 底部优惠 end -->
  </header>
</template>

<script>
export default {
  props: {
    poiInfo: {
      type: Object,
      default () {
        return {}
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header{
  height: 140px;
  padding: 20px 0 0;
}
.top-wrap{
  display: flex;
  align-items: center;
  height: 31px;
  line-height: 31px;
  .back{
    width: 50px;
    text-align: center;
  }
  .share-box{
    width: 100px;
    text-align: center;
    line-height: 31px;
    font-size: 0;
    a{
      display: inline-block;
      font-size: 0;
      margin: 0 3px;
      text-decoration: none;

      &.pinon{
        span{
          padding: 2px;
          font-size: 14px;
          border: 1px solid #232323;
          color: #232323;
        }
      }
      &.share{
        i{
          display: inline-block;
          width: 4px;
          height: 4px;
          border-radius: 50%;
          border: 1px solid #232323;
          margin: 0 1px;
        }
      }
    }
  }
  .search-box{
    flex: 1;
    position: relative;
    i{
      position: absolute;
      width: 20px;
      height: 20px;
      left: 10px;
      background: url('/static/img/search.png') no-repeat center center;
      background-size: contain;
      top: 50%;
      transform: translateY(-50%);
    }
    input{
      display: block;
      width: 100%;
      height: 31px;
      padding-left: 40px;
      border: none;
      outline: none;
      background-color: #f5f5f5;
      box-sizing: border-box;
      border-radius: 50px;
    }
  }
}
</style>
