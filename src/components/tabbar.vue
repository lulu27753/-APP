<!-- 实现tab的外层容器 -->
<template>
	<div class="m-tabbar"><slot></slot></div>
</template>

<script>
	
</script>

<style lang="less">
	.m-tabbar{
		display: -webkit-flex;
		display: -moz-flex;
		display: -ms-flex;
		display: -o-flex;
		display: flex;
		display-direction: row;
		position: fixed;
		bottom: 0;
		left: 0;
		right: 0;
		width: 100%;
		height: 50px;
		overflow: hidden;
		background: #fff;
		border-top: 1px solid #e4e4e4;


	}
</style>