<template>
    <div class="navbar navbar-default topnav">
        <div class="container">
            <div class="navbar-header">
                <a href="/" class="navbar-brand">
                    <img :src="logo.src" :alt="logo.title">
                    <span class="title">{{ logo.title }}</span>
                </a>
            </div>

            <div id="top-navbar-collapse" class="collapse navbar-collapse">
                <ul class="nav navbar-nav">
                    <li v-for="item in navList">
                        <a href="#">{{ item }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TheHeader',
    data() {
        return {
            logo: {
                src: `${this.uploadsUrl}upload/images/logo.82b9c7a5.png`,
                title: 'Learnku Vue.js'
            },
            navList: ['社区', '头条', '问答', '教程']
        }
    },
    beforeCreate() {
        this.uploadsUrl = 'http://49.235.202.233:8001/'
    }
}
</script>

<style scoped>
.title {
    /*display: none;*/
    color: #1b1a1a;
}

.navbar-brand > img {
    display: inline-block;
    margin-right: 15px;
}

</style>
