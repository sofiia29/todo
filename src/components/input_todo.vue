<template>
    <div class="inpt">
        <input :placeholder="placeholder" :class="{'is-icon':isIcon}" :value="value" @input="$emit('input', $event.target.value)">
        <img v-if="isIcon" src="./../assets/images/plus.svg">
    </div>
</template>

<script>
export default {
    name: "input_todo",
    props:{
        isIcon: {
            type: Boolean,
            default: false,
        },
        placeholder: String,
        value: String,
    },
    data(){
        return{
            content: this.value,
        }
    },
    methods:{
        handleInput (e) {
            this.$emit('input', this.content)
        }
    }
}
</script>

<style scoped>
    .inpt{
        background: #FFFFFF;
        border: 3px solid #E2BDF3;
        overflow: hidden;
        border-radius: 30px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 482px;
        padding: 7px 17px;
        box-sizing: border-box;
        margin-bottom: 60px;
    }

    input{
        font-family: 'Amatic SC';
        border: none;
        font-style: normal;
        font-weight: 400;
        font-size: 35px;
        line-height: 44px;
        width: 100%;
        color: #000000;
    }

    input:focus{
        outline: none;
    }

    @media(max-width: 700px){
        .inpt{
            width: 100%;
        }


    }
</style>