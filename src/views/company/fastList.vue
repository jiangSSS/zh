<template>
	<div class="container">
		<Header></Header>
         <section class="wb100 dis-ib conTop">
        <ul class="indexNav">
            <li>
                <a  @click="$router.push('/search')">
                    <img src="/static/images/icon-43.png">
                    <p>工商企业</p>
                </a>
            </li>
            <li>
                <a  @click="$router.push('/search')">
                    <img src="/static/images/icon-44.png">
                    <p>国家机关</p>
                </a>
            </li>
            <li>
                <a  @click="$router.push('/search')">
                    <img src="/static/images/icon-45.png">
                    <p>事业单位</p>
                </a>
            </li>
            <li>
                <a  @click="$router.push('/search')">
                    <img src="/static/images/icon-46.png">
                    <p>社会团队</p>
                </a>
            </li>
            <li>
                <a @click="$router.push('/creditBank')">
                    <img src="/static/images/icon-47.png">
                    <p>人行征信</p>
                </a>
            </li>
            <li>
                <a href="Five.asp">
                    <img src="/static/images/icon-48.png">
                    <p>五险一金</p>
                </a>
            </li>
            <li>
                <a @click="$router.push('/edu')">
                    <img src="/static/images/icon-49.png">
                    <p>学历验证</p>
                </a>
            </li>
            <li>
                <a @click="$router.push('/identity')">
                    <img src="/static/images/icon-50.png">
                    <p>身份验证</p>
                </a>
            </li>
            <li>
                <a @click="$router.push('/shop/shopInspect')">
                    <img src="/static/images/icon-62.png">
                    <p>商品抽检</p>
                </a>
            </li>
           <!-- <li>
                <a @click="$router.push('/food/food')">
                    <img src="/static/images/icon-63.png">
                    <p>食品抽检</p>
                </a>
            </li> -->
            <li>
                <a @click="$router.push('/drug/drug')">
                    <img src="/static/images/icon-65.png">
                    <p>药品抽查</p>
                </a>
            </li>
            <!-- <li>
                <a @click="$router.push('/publicUnit')">
                    <img src="/static/images/icon-63.png">
                    <p>公共单位查询</p>
                </a>
            </li> -->
            <li>
                <a @click="$router.push('/creditRepair')">
                    <img src="/static/images/icon-64.png">
                    <p>信用修复</p>
                </a>
            </li>
        </ul>
        </section>
	</div>
</template>

<script>
    import Header from "@/components/Header"
	export default {
		components: {
            Header
		},
		data() {
			return {}
		},
		methods:{},
		created(){}
	}
</script>

<style scoped>
	
</style>
