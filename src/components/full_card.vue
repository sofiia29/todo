<template>
    <div class="backgr">
        <h1>To Do List:</h1>
        <Input_todo placeholder="what do you want to do?" isIcon="true"></Input_todo>
        <Input_todo placeholder="search" v-model="searchRequest"></Input_todo>
        {{searchRequest}}
        <div v-for="item in todos" v-bind:key="item.id">
            <One_task :item="item"></One_task>
        </div>
        
    </div>
</template>

<script>
import Input_todo from './../components/input_todo.vue';
import One_task from './one_task.vue';
import axios from 'axios';
export default {
    name: "full_card",
    components:{
    Input_todo,
    One_task
}, 
    data(){
        return{
            file: null,
            todos: null,
            searchRequest: "some txt",
        }
    },
    methods:{
        forSearch(todos){
            let result = todos.filter(todo => todo.name.includes('t'));
            console.log(result);
        }
    },
    mounted(){
    axios.get('http://127.0.0.1:54321/').then(response => {
        console.log(response)
        this.todos = response.data
        this.forSearch(this.todos)})
    }
}
</script>

<style scoped>
    .backgr{
        background-color: #A360C2;
        box-sizing: border-box;
        width: 100%;
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

    @media(max-width: 700px){
        h1{
            text-align: center;
        }

        .backgr{
            align-items: center;
            width: auto;
            margin: 20px;
        }
        
    }
</style>