
<template>
  <div class="Globals">
    <el-row class="health-top">
      <el-col :span="4" class="search-box displayTable">
        <p class="teableCell">
          <span></span>
        </p>
      </el-col>
      <el-col :span="16" class="health-name displayTable">
        <div class="grid-content bg-purple">
          <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="体检套餐" name="third">
              <List></List>
            </el-tab-pane>
            <el-tab-pane label="体检机构" name="fourth">
              <InstitutionalList></InstitutionalList>
            </el-tab-pane>
          </el-tabs>
        </div>
      </el-col>
      <el-col :span="4" class="viewtype-switch displayTable">
        <p class="teableCell">
          <span></span>
        </p>
      </el-col>
    </el-row>
    <Foot></Foot>
  </div>
</template>

<script>
import Foot from '../footer/footer'
import List from './packsList'
import InstitutionalList from '../Institutional/InstitutionalList'
export default {
  name: 'packageList',
  data() {
    return {
      activeName: 'third'
    };
  },
  components: {
    Foot,
    List,
    InstitutionalList
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    }
  }
};
</script>
<style >
.el-tabs__header {
  border: none;
}
	/* 设置默认值  */
	.Globals{height: 100%;background: #FFFFFF;font-size: 14px;}
	.health-top{position: relative;border-bottom: 1px solid #EDEEEF;text-align: center;font-size: 0.8rem;height: 8%;}
	.health-top .health-name{font-size: 16px;}
	.health-top .search-box, .health-top .health-name, .health-top .viewtype-switch{height: 100%;}
	.health-top .search-box p span{display:block;width:100%;height:100%; background: url(../../assets/images/health/search.png)no-repeat center;background-size: 29%;}
	.health-top .viewtype-switch p span{display:block;width:100%;height:100%; background: url(../../assets/images/health/qh1.png)no-repeat center;background-size: 32%;}


	/*垂直居中*/
	.displayTable{display: table;}
	.displayTable .teableCell{display: table-cell;vertical-align: middle;}
</style>
