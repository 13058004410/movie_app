<template>
    <div class="login">
        <p>
            <input type="text" placeholder="请输入帐号">
        </p>
        <p>
            <input type="text" placeholder="请输入密码">
        </p>
        <p>
            <input type="submit" value="登陆">
        </p>
    </div>
</template>

<script>
export default {
    name:'login'
}
</script>

<style>
.login p{text-align: center;}
.login p input{line-height:60px;width:100%;text-align: center;font-size:35px}
</style>