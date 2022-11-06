<template>
    <div class="task">
        <p>Some text</p>
        <p>21.10.2022 14:30</p>
        <div class="buttons">
            <Purple_button>Edit</Purple_button>
            <Purple_button>Delete</Purple_button>
        </div>
        
    </div>
</template>

<script>
import Purple_button from './purple_button.vue';
export default {
    components: { Purple_button }
}
</script>

<style scoped>
    p{
        font-style: normal;
        font-weight: 700;
        font-size: 30px;
        line-height: 38px;
        color: white;
        margin: 0;
    }

    .task{
        display: flex;
        flex-direction: row;
        border-bottom: 1px solid #E2BDF3;
        justify-content: space-between;
        padding-bottom: 27px;
        align-items: center;
    }

    .buttons{
        display: flex;
        flex-direction: row;
        gap: 60px;
    }
</style>