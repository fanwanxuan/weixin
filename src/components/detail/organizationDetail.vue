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
				<span class="teableCell">机构详情</span>
			</el-col> 
			<el-col :span="4"></el-col>
		</el-row> 
		<!--detail-box -->
		<div class="detail-box">
			<div class="detail-box-info">
				<div class="info-img">
					<img src="../../assets/images/detail/detail-img.png" />
				</div>
				<div class="info-box">
					<span class="">成都八一军区骨科体检医院</span>
					<span class="">公立医院</span>
				</div>
			</div>
			
		</div>  
	</div>
</template>

<script>
	export default {
		name:'organizationDetail' 
	}
</script>

<style>
	.Globals{background: #F5F5F5;}
	.detail-box-info .info-img img{display:block;width: 100%;}
	.info-box{padding: 3% 4%;background: #FFFFFF;font-weight: bold;font-size: 15px;}
	
	
	
	
	
	
	
</style>