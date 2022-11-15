<template>
    <div>
        <label class="container">
            <input type="checkbox" id="check" name="check">
            <span class="custom"></span>
            Some text
        </label>
    </div>
</template>

<script>
export default {
    name: "custom_check",

}
</script>

<style scoped>
    .container{
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 27px;
        margin: 0;
        width: auto;
    }

    #check{
        display: none;
    }

    .custom{
        display: inline-block;
        width: 25px;
        height: 25px;
        background-color: #A360C2;
        border: 1px solid #E2BDF3;
        border-radius: 50%;
    }

    input:checked+.custom{
        background-image: url(./../assets/images/check.svg);
        background-size: 105% 105%;
        background-position: center;
    }

    label{
        font-style: normal;
        font-weight: 700;
        font-size: 30px;
        line-height: 38px;
        color: white;
        margin: 0;
        
    }

</style>