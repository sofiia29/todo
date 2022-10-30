<template>
    <div>
        <button>{{txt}}</button>
    </div>
</template>

<script>
export default {
    name: "purple_button",
    props:{
        txt: String,
    },
}
</script>

<style scoped>
    button{
        width: 95px;
        height: 30px;
        background: #E2BDF3;
        border-radius: 30px;
        font-style: normal;
        font-weight: 700;
        font-size: 30px;
        line-height: 38px;
        color: white;
        text-align: center;
    }
</style>