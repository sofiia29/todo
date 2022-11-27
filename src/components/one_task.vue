<template>
    <div class="task">
        <Custom_check :name = "item.name"></Custom_check>
        <p>{{dataFormat(item.time)}}</p>
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
    components: { Purple_button, Custom_check },
    props:{
        item:{
            type: Object,
            required: true, 
        },
    },

    methods: {
        dataFormat(data){
            let dates = new Date(data);
            let day = dates.getDate();
            if(day < 10){
                day = "0" + day;
            };

            let month = dates.getMonth();
            if(month < 10){
                month = "0" + month;
            };

            let year = dates.getFullYear();

            let hours = dates.getHours();
            if(hours < 10){
                hours = "0" + hours;
            };

            let min = dates.getMinutes();
            if(min < 10){
                min = "0" + min;
            };

            let sec = dates.getSeconds();
            if(sec < 10){
                sec = "0" + sec;
            };
            return day + "." + month + "." + year + "  " + hours + ":" + min + ":" + sec;
            
        }
    }

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