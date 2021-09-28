<template>
        <div class="login">
            <label>
                <span>用户名：</span>
                <input v-model="username" @change="setUser"/>
            </label>
        </div>
</template>

<script>
    export default {
        name: "loginDiv",

        data() {
            return {
                username: ''
            }
        },
        methods: {
            setUser: function () {
                this.$emit('transferUser', this.username)
            }
        }
    }

</script>

<style scoped>

</style>
