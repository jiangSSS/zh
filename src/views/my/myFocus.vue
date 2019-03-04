<template>
	<div>
		<Header></Header>
		<img src="/static/images/icon-35.png" class="logo">
		<div>
			<ul class="HeadlinesList" v-infinite-scroll="loadMore" infinite-scroll-disabled="loading">
				<li class="itemAll" v-for="(item,index) in pageList" :key="index">
					<div class="clearfix companyLine">
						<span class="company fl">{{item}}</span><span class="cancle fr">取消关注</span>
					</div>
				</li>
			</ul>
		</div>
	</div>
</template>

<script>
	import Header from "@/components/Header"
	export default {
		components: {
			Header
		},
		data() {
			return {
				pageList: ["北京阿里巴巴科技有限公司", "北京阿里巴巴科技有限公司", "北京阿里巴巴科技有限公司", "北京阿里巴巴科技有限公司", ]
			}
		},
		methods: {
			loadMore() {

			},
			getData() {

			}
		},
		created() {}
	}
</script>

<style scoped>
	.focusItem {
		padding: .5rem;
		background: #fff;
	}

	.HeadlinesList {
		margin-top: 1.5rem;
	}

	.companyLine {
		padding: .4rem .5rem;
		margin-bottom: .2rem;
		background: #fff;
	}

	.itemAll:first-child {
		border-top: 1px solid #f3f5f7
	}

	.company {
		font-size: .5rem;
		font-weight: 400;
		color: #333;
	}

	.cancle {
		font-size: .5rem;
		color: #ccc;
	}
</style>
