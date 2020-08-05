<template>
	<view class="main">
		<view class="header">
			<view class="position">
				<u-icon name="map" size="40" color="white"></u-icon>
				<text class="text">{{position.address}}</text>
			</view>
			<view class="message">
				<u-icon name="chat" size="40" color="white"></u-icon>
				<u-badge type="error" :count="message.badge" color="white" size="mini" :offset="message.offset"></u-badge>
			</view>
		</view>
		<view class="search">
			<view class="input">
				<u-search :show-action="false" height="60" bg-color="white" placeholder="搜索附近商家摊位商品" :clearabled="false"></u-search>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				position: {
					address: "山东省烟台市蓝海路创业1号孵化器"
				},
				message: {
					badge: 3,
					offset: [-10, -10]
				}
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.main {
		display: flex;
		flex-direction: column;
		height: 100%;

		.header {
			height: 80upx;
			width: 100%;
			background-color: #FF9500;
			display: flex;
			flex-direction: row;
			align-items: center;

			.position {
				height: 80upx;
				margin-left: 20upx;
				width: 60%;
				display: flex;

				.text {
					width: 80%;
					margin-left: 10upx;
					color: white;
					font-family: $text-font-family;
					font-size: 30upx;
					line-height: 80upx;
					text-overflow: ellipsis;
					white-space: nowrap;
					overflow: hidden;
				}
			}

			.message {
				position: fixed;
				right: 20upx
			}
		}

		.search {
			width: 100%;
			height: 80upx;
			background-color: #FF9500;

			.input {
				width: 710upx;
				margin-left: 20upx;
			}
			
		}
	}
</style>
