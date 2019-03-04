<template>
	<div class="container">
		<Header></Header>
		<section class="wb100 dis-ib conTop">
			<div class="loginList">
				<ul :model="formData">
					<li>
						<input type="text" v-model="formData.mobile" placeholder="请输入手机号码">
					</li>
					<li>
					<!-- 	<van-cell-group>
							<van-field v-model="formData.code" center clearable placeholder="验证码">
								<van-button slot="button" size="small" type="primary" class="submit">获取验证码</van-button>
							</van-field>
						</van-cell-group> -->
						<input type="text" class="codeInput" v-model="formData.code" placeholder="请输入验证码"><span class="getCode">获取验证码</span>
					</li>
					<li>
						<input type="text" v-model="formData.newPwd" placeholder="设置新密码">
					</li>
				</ul>
			</div>
			<div class="wb100 dis-ib tc mtb5">
				<a @click="submit" class="BtnSmall">提交</a>
			</div>
		</section>
	</div>
</template>

<script>
	import Header from "@/components/Header.vue";
	import {
		Toast
	} from "mint-ui"
	export default {
		components: {
			Header
		},
		data() {
			return {
				formData: {
					mobile: "",
					code: "",
					newPwd: ""
				}
			}
		},
		methods: {
			submit() {
				this.formData.mobile = ""
				this.formData.code = ""
				this.formData.newPwd = ""
				let instance = Toast('修改成功');
				setTimeout(() => {
					instance.close();
				}, 2000);
			}
		},
	}
</script>

<style scoped>
	.forget {
		color: #999
	}

	/* .loginList {
        margin-top: 1.4rem
    } */

	.loginList li {
		border: none
	}

	/* .loginList li input {
        border: 1px solid #ccc;
        height: 1.2rem;
        padding: .3rem;
    } */
	.submit {
		background: #e70000;
		border-color: #e70000
	}

	/deep/ .van-button {
		width: 100%;
	}

	/deep/ .van-cell {
		padding: .1rem
	}

	/* /deep/ .van-cell--center {
        border: 1px solid #ccc
    } */
	/deep/ .van-field__control {
		padding: .3rem
	}

	.forget {
		color: #409eff;
		padding: .15rem .05rem
	}
	.codeInput{
		width: 65%!important;
		padding-right: 1rem;
	}
	.getCode{
		background: #e70000;
		padding: .2rem .3rem;
		color: #fff;
		border-radius: 6%;
	}
</style>
