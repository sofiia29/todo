<template>
    <div class="task">
        <Custom_check></Custom_check>
        <p>21.10.2022 14:30</p>
        <div class="buttons">
            <Purple_button>Edit</Purple_button>
            <Purple_button>Delete</Purple_button>
        </div>
        
    </div>
</template>

<script>
import Purple_button from './purple_button.vue';
import Custom_check from './custom_check.vue';
export default {
    components: { Purple_button, Custom_check }
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

    @media(max-width: 700px){
        .task{
            flex-direction: column;
            gap: 20px;
        }
    }
</style>