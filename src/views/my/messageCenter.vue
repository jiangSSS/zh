<template>
	<div>
		<Header></Header>
		<img src="/static/images/icon-35.png" class="logo">
		<div>
			<ul class="HeadlinesList" v-infinite-scroll="loadMore" infinite-scroll-disabled="loading">
				<li class="itemAll" v-for="(item,index) in pageList" :key="index">
					<div class="companyLine">
						<div class="company">{{item.title}}</div>
						<div class="clearfix">
							<div class="content fl">{{item.content}}</div>
							<div class="time fr">{{item.time}}</div>
						</div>
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
				pageList: [{
						title: "企信网祝您春节快乐！",
						content: "系统消息",
						time: "2018-04-12 07:48"
					},
					{
						title: "企信网祝您春节快乐！",
						content: "系统消息",
						time: "2018-04-12 07:48"
					},
					{
						title: "企信网祝您春节快乐！",
						content: "系统消息",
						time: "2018-04-12 07:48"
					},
				]
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
		border-bottom: .3rem solid #fafafa
	}

	.HeadlinesList {
		margin-top: 1.5rem;
	}

	.companyLine {

		padding: .3rem .5rem;
	}

	.HeadlinesList li {
		background: #fff;
		margin-bottom: .2rem
	}

	.itemAll:first-child {
		border-top: 1px solid #fafafa
	}

	.company {
		font-weight: 400;
		font-size: .44rem;
		color: #444;
	}

	.content {
		color: #777;
		padding: .2rem 0;
	}

	.time {
		color: #999;
		padding: .2rem 0;
	}

	.cancle {
		font-size: .5rem;
		font-weight: 700;
		color: #ccc;
	}
</style>
