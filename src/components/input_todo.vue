<template>
    <div class="inpt">
        <input placeholder="things you want to do today?">
        <img src="./../assets/images/plus.svg">
    </div>
</template>

<script>
export default {
    name: "input_todo",
}
</script>

<style scoped>
    .inpt{
        background: #FFFFFF;
        border: 3px solid #E2BDF3;
        border-radius: 30px;
    }

    input{
        font-style: normal;
        font-weight: 400;
        font-size: 35px;
        line-height: 44px;
        color: #000000;
    }
</style>