<template>
	<div class="container">
		<Header></Header>
		<img src="/static/images/icon-35.png" class="logo">
		<div class="marginTop">
			<div class="userList">
				<ul :model="formData">
					<li class="clearfix">
						<span class="fl">企业名称：</span>
						<input class="fr tr" type="text" placeholder="请输入企业名称">
					</li>
					<li class="clearfix">
						<span class="fl">联系电话：</span>
						<input class="fr tr" type="text" placeholder="请输入电话号码">
					</li>
					<li class="clearfix">
						<span class="fl">邮箱：</span>
						<input class="fr tr" type="text" placeholder="请输入联系邮箱">
					</li>
					<li class="clearfix">
						<span class="fl">企业网址：</span>
						<input class="fr tr" type="text" placeholder="请输入企业网址">
					</li>
					<li class="clearfix">
						<span class="fl">公司地址：</span>
						<input class="fr tr" type="text" placeholder="请输入公司地址">
					</li>
					<li class="clearfix">
						<span class="fl">公司简介：</span>
						<input class="fr tr" type="textarea" rows="3" placeholder="请填写公司描述">
					</li>
					<li class="clearfix">
						<span class="fl">荣誉资质：</span>
						<input class="fr tr" type="text">
						<!-- <van-uploader :after-read="onRead">
							<van-icon name="photograph" />
						</van-uploader> -->
					</li>
				</ul>
				<!-- <div><van-radio class="read" checked-color="#e50015">我已经阅读并同意《认证服务协议》</van-radio></div> -->
				<!-- <van-checkbox class="read" v-model="checked">我已经阅读并同意《认证服务协议》</van-checkbox> -->
				<van-button class="submit" @click="submit">保存</van-button>
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
				formData: {
					company: "",
					idCard: "",
					name: "",
					mobile: "",
					email: "",
				},
				checked: false
			}
		},
		methods: {
			submit() {
				this.$router.push("/attestationList")
			}
		},
		created() {}
	}
</script>

<style scoped>
	.read {
		font-size: .38rem;
		color: #ccc;
		padding: .4rem .4rem;
	}

	/deep/ .van-radio__label {
		color: #999;
	}

	.userList li {
		margin: 0rem .4rem;
		border-bottom: 1px solid rgb(241, 241, 241);
		padding: .3rem 0;
	}

	.marginTop {
		border-top: 1px solid rgb(241, 241, 241)
	}

	.userList li span {
		font-family: "Microsoft YaHei";
		color: #444;
		font-size: .44rem;
		display: inline-block;
		line-height: .9rem;
		/* width: 2.4rem */
	}

	.userList li input {
		height: .9rem;
		width: 7rem;
		overflow: hidden;
		line-height: .7rem;
		font-size: .44rem;
		color: #383838;
		font-family: inherit;
		margin: 0;
		padding: 0 .15rem;
		background: #fff
			/* border: 1px solid #ccc; */
	}

	/deep/ .van-checkbox__icon--checked .van-icon {
		background: #e50015;
		border-color: #e50015;
	}

	.submit {
		color: #fff;
		background: #e50015;
		width: 100%;
		position: absolute;
		bottom: 0;
	}
</style>
