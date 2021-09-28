<template>
    <header class="header">
        <div>{{logo}}</div>
        <ul>
            <span id="s1" v-for="nav in navs">{{nav.li}}</span>
            <el-row>
                <el-button>默认按钮</el-button>
                <el-button type="primary">主要按钮</el-button>
                <el-button type="success">成功按钮</el-button>
                <el-button type="info">信息按钮</el-button>
                <el-button type="warning">警告按钮</el-button>
                <el-button type="danger">危险按钮</el-button>
            </el-row>
        </ul>
    </header>
</template>

<script>
    export default {
        name: "headerDiv",
        data() {
            return {
                navs: [
                    {li: '主页'},
                    {li: '日志'},
                    {li: '说说'},
                    {li: '主页'},
                    {li: '相册'},
                ]
            }
        },
        props: {
            logo: String
        }
    };
</script>

<style scoped>

</style>
