<!-- 子组件的item项 -->
<template>
	<a class="m-tabbar-item" :class="{'is-active':isActive}" @click="goToRouter">
		<span class="m-tabbar-item-icon" v-show="!isActive">
			<slot name="icon-normal"></slot>
		</span>
		<span class="m-tabbar-item-icon" v-show="isActive">
			<slot name="icon-active"></slot>
		</span>
		<span class="m-tabbar-item-text">
			<slot></slot>
		</span>
	</a>
</template>

<script>
	export default{
		props:{id:{type:String}, isRouter:{type:Boolean, default:false}},
		computed:{
			isActive(){if(this.$parent.value === this.id){return true;}}
		},
		methods:{
			goToRouter(){
				this.$parent.$emit('input', this.id)
				//判断是否为路由跳转,并根据id跳转到对应的路由页面
				if (this.isRouter) {this.$route.push(this.id)};
		}
		}
	}
	
</script>

<style lang="less">
@import "../assets/less/var.less";
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
		       		color: @tabbarActiveColor;
		      }
		 }
	}
</style>