<template>
	<header class="m-header" :class="{'is-bg':bg, 'is-fixed':fixed }">
		<div class="m-header-button is-left"><slot name="left"></slot> </div>
		<h1 class="m-header-title" v-text="title"></h1>
		<div class="m-header-button is-right"><slot name="right"></slot></div>
	</header>
</template>
<script>

	export default{
		props:{
			title:{type:String, default:''},
			bg:{type:Boolean, default:false},
			fixed:{type:Boolean, default:false}
		}
	}
</script>
<style lang="less">

/* 导入颜色变量 */
@import url('../assets/less/var.less');
.m-header{
	display: -webkit-flex;
	display: -moz-flex;
	display: -ms-flex;
	display: -o-flex;
	display: flex;
	-ms-align-items: center;
	align-items: center;
	height: 44px;
	padding: 0 10px;
	background: #fff;
	color: @headerDefaultColor;
	border-bottom: 1px solid #eee;

	a{color: @headerDefaultColor;}
	.m-header-button{
	width: 70px;
	-ms-align-items: stretch;
	align-items: stretch;
	&.is-left{text-align: left;}
	&.is-right{text-align: right;}
	.m-icon-img{width: 20px; height: 20px;}
	.margin-right-10{margin-right: 10px;}
	.m-header-button{
			flex:1;
			text-align: center;
			font-size: 16px;
			-ms-text-overflow: ellipsis;
			text-overflow: ellipsis;
			white-space: nowrap;
			overflow: hidden;

		}

	}
	&.is-bg{
		/* 是否显示背景色，默认是绿色 */
		background: @headerBg;
		color: #fff;
		a{color: #fff;}
		.m-header-title{
	            color: #fff;
	        }
	}

	&.is-fixed{
		/* 是否显示在顶部 */
		position: fixed;
		left: 0;
		top: 0;
		z-index: 0;

	}

}

</style>