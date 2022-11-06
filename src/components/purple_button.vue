<template>
    <div>
        <button><slot></slot></button>
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
        font-family: 'Amatic SC';
        /* width: 95px;
        height: 30px; */
        padding: 3px 20px;
        background: #E2BDF3;
        border-radius: 30px;
        font-style: normal;
        font-weight: 700;
        font-size: 30px;
        line-height: 38px;
        color: white;
        text-align: center;
        border: none;
    }
</style>