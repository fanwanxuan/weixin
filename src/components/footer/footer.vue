<template>
<div class='footer'>
  <!-- 底部 -->
  <div class="guide_item">
    <router-link active-class='on' :to='{path:"/index"}'>
      <i class='icon iconfont icon-shouyeziji01 icon_style'>
        <use  :xlink:href="$route.path.indexOf('/') !== -1? '#msiteActive' : '#msite'"></use>
      </i>
      <span>首页</span>
    </router-link>

  </div>
  <div class="guide_item">
     <router-link active-class='on' :to='{path:"/packageList"}'>
    <!-- <svg class="icon_style"> -->
    <i class='icon iconfont icon-goumaichesuo'>
      <use :xlink:href="$route.path.indexOf('packageList') !== -1? '#findActive' : '#find'" style="border:1px red solid">1111</use>
    </i>
    <!-- </svg> -->

    <span>体检购买</span>
      </router-link>
  </div>
  <div class="guide_item">
     <router-link active-class='on' :to='{path:"/healthProduct"}'>
    <i class='icon iconfont  icon-chanpin'>
      <use  :xlink:href="$route.path.indexOf('healthProduct') !== -1? '#orderActive' : '#order'"></use>
    </i>
    <span>健康产品</span>
     </router-link>
  </div>
  <div class="guide_item">
     <router-link active-class='on' :to='{path:"/personalCenter"}'>
    <i class='icon iconfont icon-gerenzhongxin'>
                    <use :xlink:href="$route.path.indexOf('personalCenter') !== -1? '#profileActive' : '#profile'"></use>
               </i>
    <span>个人中心</span>
     </router-link>

  </div>
  <!-- 底部 -->
</div>
</template>

<script>
export default {
  name: 'footer',
  data() {
    return {

    }
  },
  mounted() {
    // this.flag1 = true;
  },
  methods: {

  },
  beforeRouteUpdate(to, from, next) {

    next(vm => {
      // 通过 `vm` 访问组件实例
      this.gotoAddress('/', 1);
      this.$router.push(path);
      alert(111);
    })
  }
}
</script>

<style>
.footer {
  width: 100%;
  background: #fff;
  position: fixed;
  bottom: 0;
  height: 49px;
  padding: 5px 0;
  font-size: 14px;
}

.guide_item {
  flex: 1;
  float: left;
  width: 25%;
  height: 100%;
  display: flex;
  text-align: center;
  flex-direction: column;
  align-items: center;
}

.icon_style {
  fill: #ccc;
}

.on {
  color: #17aae7!important;
}
/* 首页 图标 */
.on .icon-shouyeziji01:before {
  content: "\e69f";
}
/* 购买 图标 */
.on .icon-goumaichesuo:before {
  content: "\e6a5";
}
/* 健康 图标 */
.on .icon-chanpin:before {
  content: "\e63f";
}
/* 个人中心 图标 */
.on .icon-gerenzhongxin:before {
  content: "\e61f";
}

a{
  color:#333;
 text-decoration:none;
}
a i{
  display:block;
}
</style>
