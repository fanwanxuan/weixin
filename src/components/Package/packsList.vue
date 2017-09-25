<template>
  <div class='packIF'>

    <el-row :gutter="20">
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
       <hr/>
    </el-row>
       <pack></pack>
  </div>
</template>

<script>
import pack from '../index/pack'
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
    &:last-child {
      margin-bottom: 0;
    }

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
    left: -44px;
    right: -44px;
  }
  /* 水平线 */
  hr{
     border-color:#e2e4e5;
     margin-left: -5px;
     width: 103%;
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
</style>
