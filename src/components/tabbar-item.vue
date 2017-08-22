<!-- 子组件的item项 -->
<template>
	<a class="m-tabbar-item">
		<span class="m-tabbar-item-icon">
			<slot name="icon-normal"></slot>
		</span>
		<span class="m-tabbar-item-text">
			<slot></slot>
		</span>
	</a>
</template>

<script>
	
</script>

<style lang="less">
	.m-tabbar-item{
		-webkit-flex: 1;
		-moz-flex: 1;
		-ms-flex: 1;
		-o-flex: 1;
		flex: 1;
		text-align: center;
		.m-tabbar-item-icon{
			display: block;
			padding-top: 2px;
			img{
		              width: 28px;
		              height: 28px;
		          }
		}
		.m-tabbar-item-text{
	          display: block;
	          font-size: 10px;
	          color:#949494;
	      }
		 &.is-active{
		      .m-tabbar-item-text{
		       		color: #42bd56;
		      }
	}
</style>