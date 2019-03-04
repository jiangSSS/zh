<template>
	<div>
		<Header></Header>
		<div class="marginTop listBox" v-infinite-scroll="loadMore" infinite-scroll-disabled="loading">
			<div class="pageListBox" v-for="(item,index) in pageList" :key="index">
				<div @click="$router.push('/attestations')">
					<div class="searchListTop">
						<div class="photo">
							<img src="/static/images/logo/logo3.png">
						</div>
						<div class="clearfix">
							<h5 class="title fl">{{item.ENTNAME}}</h5>
							<div class="info fr">
								<span>信用查认证</span>
							</div>
						</div>
						<span class="label">{{item.label}}</span>
					</div>
					<div class="searchListBottom">
						<span class="labelList">
							<em>法定代表人</em>
							<i class="c-e70016" v-if="item.NAME">{{item.NAME}}</i>
							<i v-else>---</i>
						</span>
						<span class="labelList">
							<em>注册资本</em>
							<i v-if="item.REGCAP">{{item.REGCAP}}</i>
							<i v-else>---</i>
						</span>
						<span class="labelList">
							<em>成立日期</em>
							<i v-if="item.REGCAP">{{item.ESDATE}}</i>
							<i v-else>---</i>
						</span>
					</div>
				</div>
			</div>
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
						title: "腾讯科技（上海）有限公司",
						label: "在业",
						low1: "奚丹",
						low2: "500万美元",
						low3: "2008-07-23",
						img: "/static/images/logo/logo-1.png"
					},
					{
						title: "腾讯科技（上海）有限公司",
						label: "在业",
						low1: "奚丹",
						low2: "500万美元",
						low3: "2008-07-23",
						img: "/static/images/logo/logo-1.png"
					},
				],
			}
		},
		methods: {
			loadMore() {

			},
			getData() {
				// this.$axios.post(`/solr/qst_entfind_new/select`,{params:{'q':'*','indent':'true','wt':'json'}}).then(res=>{
				this.$axios.post(`/solr/qst_entinfobypripid/select`, {
					params: {
						'q': '*',
						'indent': 'true',
						'wt': 'json'
					}
				}).then(res => {
					console.log("1", res)
					this.pageList = res.response.docs
				})
			},
		},
		created() {
			this.getData()
		}
	}
</script>

<style scoped>
	.pageListBox {
		width: 100%;
		display: block;
		background: #fff;
		margin-bottom: .2rem;
		overflow: hidden;
	}
	.searchListTop .info span{
		margin-top: .2rem;
	}
	.searchListTop .title{
		max-width: 70%;
	}
</style>
