<template>
	<div class="Globals">
		<!-- 头部 -->
		<el-row class="health-top">
			<el-col :span="4" class="search-box displayTable">
				<p class="teableCell">
					<i class="icon iconfont icon-fanhui" style="font-size: 20px;"></i> 
				</p>
			</el-col>
			<el-col :span="16" class="health-name displayTable">
				<span class="teableCell">套餐详情</span>
			</el-col> 
			<el-col :span="4"></el-col>
		</el-row>  
		<!--detail-box -->
		<div class="detail-box"></div> 
	</div>
</template>

<script>
	export default {
		name:'PackageDetail' 
	}
</script>

<style>
</style>