<template>
  <nav>
      <router-link class='nav-item' to='/goods'>
        <span>
            点餐
        </span>
      </router-link>
      <router-link class='nav-item' to='/ratings'>
        <span>
            评价
        </span>
      </router-link>
      <router-link class='nav-item' to='/seller'>
        <span>
            商家
        </span>
      </router-link>
  </nav>
</template>

<script>
export default {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
nav{
    display: flex;
    height: 40px;
    border-bottom: 1px solid #ccc;
    .nav-item{
        position: relative;
        flex: 1;
        text-align: center;
        line-height: 40px;
        font-size: 13px;
        color: #666;
        text-decoration: none;
        &.active{
            color: #ffbb22;
            span::after{
                content: "";
                position: absolute;
                width: 100%;
                bottom: 0;
                left: 0;
                height: 2px;
                background-color: #ffbb22;
            }
        }
        span{
            position: relative;
            display: inline-block;
            height: 100%;
        }
    }
}
</style>
