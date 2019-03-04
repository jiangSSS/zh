<template>
    <div>
        <Header></Header>
        <div class="statisticsResult publicUnitListTip">搜索到符合条件的社会组织共<i class="c-e70016">18</i>个
            <a href="JavaScript:;" class="scree">筛选</a>
        </div>
        <div id="publicUnitList" class="searchListMargin publicUnitListTop">
            <div class="">
                <ul class="publicUnitList mainHref">
                    <li>
                        <a @click="$router.push('/publicDetail')">
                            <div class="title">
                                <span>中国互联网金融协会</span>
                                <em class="c-e70016">正常</em>
                            </div>
                            <div class="label">
                                <div class="labelList">
                                    <span>统一社会信用代码</span>
                                    <em>51100000MJ0000632D</em>
                                </div>
                                <div class="labelList">
                                    <span>社会组织类型</span>
                                    <em>社会团体</em>
                                </div>
                                <div class="labelList">
                                    <span>法定代表人</span>
                                    <em>李希贵</em>
                                </div>
                            </div>
                        </a>
                    </li>
                    <li>
                        <a @click="$router.push('/publicDetail')">
                            <div class="title">
                                <span>中国互联网金融协会</span>
                                <em class="c-ff7e00">注销</em>
                            </div>
                            <div class="label">
                                <div class="labelList">
                                    <span>统一社会信用代码</span>
                                    <em>51100000MJ0000632D</em>
                                </div>
                                <div class="labelList">
                                    <span>社会组织类型</span>
                                    <em>社会团体</em>
                                </div>
                                <div class="labelList">
                                    <span>法定代表人</span>
                                    <em>李希贵</em>
                                </div>
                            </div>
                        </a>
                    </li>
                    <li>
                        <a @click="$router.push('/publicDetail')">
                            <div class="title">
                                <span>中国互联网金融协会</span>
                                <em class="c-999">撤销</em>
                            </div>
                            <div class="label">
                                <div class="labelList">
                                    <span>统一社会信用代码</span>
                                    <em>51100000MJ0000632D</em>
                                </div>
                                <div class="labelList">
                                    <span>社会组织类型</span>
                                    <em>社会团体</em>
                                </div>
                                <div class="labelList">
                                    <span>法定代表人</span>
                                    <em>李希贵</em>
                                </div>
                            </div>
                        </a>
                    </li>
                </ul>
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
            return {}
        },
        methods: {},
        created() { }
    }
</script>

<style scoped>

</style>