<template>
  <div class='packIF'>
    <el-row :gutter="20" class='marginAll'>
      <el-col :span="6">
        <div class="grid-content bg-purple">类别<i class='icon iconfont icon-icondown'></i></div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">地区<i class='icon iconfont icon-icondown'></i></div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">性别<i class='icon iconfont icon-icondown'></i></div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content bg-purple">价格<i class='icon iconfont icon-icondown'></i></div>
      </el-col>
    </el-row>
       <pack></pack>
  </div>
</template>

<script>
import pack from '../index/pack'
import homeMenu from '../../assets/css/homeMenu/homeMenu.css'
export default {
  name: 'packList',
  components:{
    pack
  }
}
</script>
<style>
 .el-row {
    margin-bottom: 20px;
      }
  .el-col {
    border-radius: 4px;
  }
.el-tabs__content {
    overflow: inherit;
    position: relative;
}
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }

  /* packIF */
   .packIF{
    position: absolute;
    top: 0;
    left:0;
    right:0;
    text-align:center;
  }

  /* active */
   .el-tabs__item.is-active {
    color: #202121;
}
.el-tabs__active-bar {
    position: absolute;
    bottom: 0;
    left: 28px;
    width: 27px!important;
    height: 3px;
    background-color: #20a0ff;
    z-index: 1;
    transition: transform .3s cubic-bezier(.645,.045,.355,1);
    list-style: none;
}
  /* 重置element样式 */
  /* .packTab {
    padding: 0 29px;
    height: 50px;
    box-sizing: border-box;
    line-height: 46px;
    display: inline-block;
    list-style: none;
    font-size: 14px;
    color: #a7acaf;
    position: relative;
} */
   .el-tabs__content {
    overflow: inherit!important;
    position: static!important;

  }
   .el-tabs-chongzhi .el-tabs__header {
   border-bottom:none!important;
  }
  .el-tabs__active-bar{
        position: absolute;
    bottom: 0;
    left: 41px;
    background-color: #1bb3f5;
}
/* 调样式 */
.el-tabs__nav,.el-tabs__header{

  width:100%;
  text-align:center;
}
.el-tabs__item{
  width:50%;
  padding:0;
  font-size:17px;
}
</style>
