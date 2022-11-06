<template>
    <div class="backgr">
        <h1>To Do List:</h1>
        <Input_todo></Input_todo>
        <One_task></One_task>
    </div>
</template>

<script>
import Input_todo from './../components/input_todo.vue';
import One_task from './one_task.vue';
export default {
    name: "full_card",
    components:{
    Input_todo,
    One_task
}
}
</script>

<style scoped>
    .backgr{
        background-color: #A360C2;
        width: 1166px;
        height: 832px;
        border-radius: 50px;
        padding: 60px;
        margin-top: 95px;
    }

    h1{
        font-style: normal;
        font-weight: 700;
        font-size: 60px;
        line-height: 76px;
        text-align: left;
        color: white;
        margin: 0;
        margin-bottom: 40px;
    }
</style>