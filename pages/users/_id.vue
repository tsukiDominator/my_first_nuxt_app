<template>
    <h1>这个页面是:{{ $route.params.id }}</h1>
</template>

<script>
export default {
    validate(data){
        return /^\d+$/.test(data.params.id)
        //此处为正则表达式，验证是否为纯数值，是则返回true
        //关于正则表达式改天再学
    }
}
</script>

